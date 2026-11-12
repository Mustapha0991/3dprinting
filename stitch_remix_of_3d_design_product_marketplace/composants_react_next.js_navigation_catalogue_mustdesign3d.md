# Composants React / Next.js — Navigation du Catalogue (MustDesign3D)

Ce document rassemble le code source complet, modulaire et typé en **TypeScript / Next.js 15+ (App Router) & Tailwind CSS** pour la navigation du catalogue de **MustDesign3D**.

Il comprend :
1. **`CatalogueNavigation.tsx`** : Barre de navigation supérieure (TopBar avec devise MAD, sélecteur FR/العربية, recherche, suivi de commande, WhatsApp et Panier interactif).
2. **`CatalogueSidebarCategories.tsx`** : Barre latérale des catégories à gauche avec compteurs d'articles, filtres de teintes 4 couleurs AMS Lite et curseur de budget MAD.
3. **`CataloguePagination.tsx`** : Barre de pagination complète (Pages 1 à 4, boutons précédent/suivant, état actif et fil d'Ariane dynamique).
4. **`types/catalogue.ts`** : Contrats de données TypeScript stricts pour les catégories, les filtres et les métadonnées de page.

---

## 1. `types/catalogue.ts` (Contrats TypeScript)

```typescript
export interface CategoryItem {
  id: string;
  name: string;
  slug: string;
  count: number;
  highlight?: boolean;
}

export interface FilamentColor {
  id: string;
  name: string;
  hex: string;
  inStock: boolean;
}

export interface CatalogueFilterState {
  category: string;
  selectedColors: string[];
  minBudget: number;
  maxBudget: number;
  sortBy: 'popular' | 'price-asc' | 'price-desc' | 'newest';
  currentPage: number;
  searchQuery: string;
}
```

---

## 2. `components/catalogue/CatalogueNavigation.tsx` (TopBar & Chrome Supérieur)

```tsx
'use client';

import React, { useState } from 'react';
import Link from 'next/link';
import { usePathname, useRouter, useSearchParams } from 'next/navigation';

interface CatalogueNavigationProps {
  cartCount?: number;
  cartTotalMad?: number;
  onOpenCart?: () => void;
}

export const CatalogueNavigation: React.FC<CatalogueNavigationProps> = ({
  cartCount = 2,
  cartTotalMad = 198,
  onOpenCart,
}) => {
  const router = useRouter();
  const searchParams = useSearchParams();
  const [searchValue, setSearchValue] = useState(searchParams.get('q') || '');
  const [lang, setLang] = useState<'fr' | 'ar'>('fr');

  const handleSearchSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    const params = new URLSearchParams(searchParams.toString());
    if (searchValue.trim()) {
      params.set('q', searchValue.trim());
    } else {
      params.delete('q');
    }
    params.set('page', '1');
    router.push(`/shop?${params.toString()}`);
  };

  return (
    <header className="w-full bg-[#fef8f4] border-b border-[#dfd9d5] sticky top-0 z-40 transition-colors">
      {/* 1. Top Ticker Banner Reassurance */}
      <div className="bg-[#1e2022] text-[#fef8f4] text-xs py-2 px-4">
        <div className="max-w-7xl mx-auto flex flex-wrap justify-between items-center gap-2">
          <div className="flex items-center gap-2">
            <span className="inline-block w-2 h-2 rounded-full bg-emerald-500 animate-pulse" />
            <span className="font-serif">
              Livraison partout au Maroc (Casablanca, Rabat, Marrakech, Tanger...)
            </span>
            <span className="opacity-40">•</span>
            <span>Paiement à la livraison (Cash on Delivery)</span>
            <span className="opacity-40">•</span>
            <span className="text-amber-300 font-medium">Bambu Lab AMS 4 Couleurs</span>
          </div>

          <div className="flex items-center gap-4 text-xs">
            <span className="font-semibold text-amber-200">MAD (DH)</span>
            <span className="opacity-30">|</span>
            <button
              onClick={() => setLang(lang === 'fr' ? 'ar' : 'fr')}
              className="hover:underline font-serif text-[11px] transition"
            >
              {lang === 'fr' ? 'العربية' : 'FR'}
            </button>
            <span className="opacity-30">|</span>
            <a
              href="https://wa.me/212661000000"
              target="_blank"
              rel="noopener noreferrer"
              className="flex items-center gap-1 text-emerald-400 hover:text-emerald-300 transition"
            >
              <svg className="w-3.5 h-3.5 fill-current" viewBox="0 0 24 24">
                <path d="M12.031 6.172c-3.181 0-5.767 2.586-5.768 5.766-.001 1.298.38 2.27 1.019 3.287l-.582 2.128 2.182-.573c.978.58 1.911.928 3.145.929 3.178 0 5.767-2.587 5.768-5.766.001-3.187-2.575-5.77-5.764-5.771zm3.392 8.244c-.144.405-.837.774-1.17.824-.299.045-.677.063-1.092-.069-.252-.08-.575-.187-.988-.365-1.739-.751-2.874-2.502-2.961-2.617-.087-.116-.708-.94-.708-1.793s.448-1.273.607-1.446c.159-.173.346-.217.462-.217l.332.007c.106.005.249-.04.39.297.144.347.491 1.2.534 1.287.043.087.072.188.014.304-.058.116-.087.188-.173.289l-.26.304c-.087.086-.177.18-.076.354.101.174.449.741.964 1.201.662.591 1.221.774 1.394.86.174.086.275.072.376-.044.101-.116.433-.506.549-.68.116-.173.231-.144.39-.086.159.058 1.011.477 1.184.564.173.087.289.13.332.202.043.073.043.419-.101.824z" />
              </svg>
              <span>Contact WhatsApp</span>
            </a>
          </div>
        </div>
      </div>

      {/* 2. Main Branding & Search Header */}
      <div className="max-w-7xl mx-auto px-4 py-4 flex flex-col md:flex-row items-center justify-between gap-4">
        {/* Brand Logo & Tagline */}
        <Link href="/" className="flex items-center gap-3 group">
          <div className="w-10 h-10 rounded-lg bg-[#1e2022] text-[#fef8f4] flex items-center justify-center font-bold text-xl shadow-sm group-hover:scale-105 transition-transform">
            M<span className="text-amber-400">3D</span>
          </div>
          <div>
            <div className="font-bold text-xl tracking-tight text-[#1e2022] flex items-center gap-1.5">
              <span>MustDesign</span>
              <span className="text-amber-600 font-extrabold text-xs px-1.5 py-0.5 rounded bg-amber-100 border border-amber-300">
                3D
              </span>
            </div>
            <p className="text-[10px] tracking-widest uppercase text-[#5a5f63] font-medium">
              Maroc • Précision Lab
            </p>
          </div>
        </Link>

        {/* Global Live Search Bar */}
        <form onSubmit={handleSearchSubmit} className="w-full md:w-96 relative">
          <input
            type="search"
            value={searchValue}
            onChange={(e) => setSearchValue(e.target.value)}
            placeholder="Rechercher un porte-clés, présentoir, lampe..."
            className="w-full pl-10 pr-4 py-2.5 rounded-full bg-white border border-[#dfd9d5] text-sm text-[#1e2022] placeholder-[#8a9094] focus:outline-none focus:ring-2 focus:ring-[#1e2022] focus:border-transparent transition shadow-inner"
          />
          <svg
            className="w-4 h-4 text-[#8a9094] absolute left-3.5 top-3.5 pointer-events-none"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
          >
            <path strokeLinecap="round" strokeLinejoin="round" strokeWidth="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
          </svg>
        </form>

        {/* Action Shortcuts & Interactive Cart */}
        <div className="flex items-center gap-3">
          <Link
            href="/order-tracking"
            className="hidden lg:flex items-center gap-1.5 text-xs text-[#5a5f63] hover:text-[#1e2022] px-3 py-2 rounded-lg border border-transparent hover:border-[#dfd9d5] transition"
          >
            <svg className="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path strokeLinecap="round" strokeLinejoin="round" strokeWidth="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2" />
            </svg>
            <span>Suivi commande</span>
          </Link>

          {/* Interactive Cart Button */}
          <button
            onClick={onOpenCart}
            type="button"
            className="flex items-center gap-3 bg-[#1e2022] hover:bg-black text-[#fef8f4] px-4 py-2.5 rounded-full shadow-sm hover:shadow transition transform active:scale-95"
            aria-label="Voir mon panier"
          >
            <div className="relative">
              <svg className="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
              </svg>
              <span className="absolute -top-1.5 -right-2 bg-amber-500 text-[#1e2022] font-black text-[10px] w-4 h-4 rounded-full flex items-center justify-center">
                {cartCount}
              </span>
            </div>
            <div className="text-left text-xs leading-none">
              <span className="opacity-70 text-[10px] block">Mon Panier</span>
              <span className="font-bold text-amber-300">{cartTotalMad} MAD</span>
            </div>
          </button>
        </div>
      </div>

      {/* 3. Primary Section Links */}
      <nav className="border-t border-[#dfd9d5] bg-white/70 backdrop-blur-sm">
        <div className="max-w-7xl mx-auto px-4 flex items-center gap-8 overflow-x-auto text-xs font-medium py-3 scrollbar-none">
          <Link href="/" className="hover:text-amber-700 whitespace-nowrap text-[#5a5f63]">
            Accueil
          </Link>
          <Link href="/shop" className="text-[#1e2022] font-bold border-b-2 border-[#1e2022] pb-1 whitespace-nowrap">
            Boutique (Catalogue)
          </Link>
          <Link href="/shop?category=gifts" className="hover:text-amber-700 whitespace-nowrap text-[#5a5f63]">
            Cadeaux Personnalisés
          </Link>
          <Link href="/shop?category=home" className="hover:text-amber-700 whitespace-nowrap text-[#5a5f63]">
            Maison & Bureau
          </Link>
          <Link href="/business" className="hover:text-amber-700 whitespace-nowrap text-[#5a5f63]">
            Professionnels (B2B)
          </Link>
          <Link href="/custom" className="hover:text-amber-700 whitespace-nowrap text-[#5a5f63] flex items-center gap-1">
            <span>Sur Mesure & 3D Lab</span>
            <span className="w-1.5 h-1.5 rounded-full bg-emerald-500" />
          </Link>
        </div>
      </nav>
    </header>
  );
};
```

---

## 3. `components/catalogue/CatalogueSidebarCategories.tsx` (Barre Latérale Gauche)

```tsx
'use client';

import React from 'react';
import { useRouter, useSearchParams } from 'next/navigation';
import { CategoryItem, FilamentColor } from '../../types/catalogue';

const DEFAULT_CATEGORIES: CategoryItem[] = [
  { id: 'all', name: 'All categories', slug: '', count: 227 },
  { id: 'decor', name: 'Décor', slug: 'decor', count: 5 },
  { id: 'desk', name: 'Desk & gaming', slug: 'desk-gaming', count: 9 },
  { id: 'keyrings', name: 'Keyrings', slug: 'keyrings', count: 24 },
  { id: 'storage', name: 'Storage', slug: 'storage', count: 7 },
  { id: 'gifts', name: 'Gifts & keepsakes', slug: 'gifts', count: 8 },
  { id: 'lamps', name: 'Lamps', slug: 'lamps', count: 25 },
  { id: 'pet', name: 'Pet accessories', slug: 'pet-accessories', count: 12 },
  { id: 'names', name: 'Names & personalised', slug: 'names', count: 18 },
  { id: 'parties', name: 'Parties & birthdays', slug: 'parties', count: 11 },
  { id: 'vases', name: 'Vases', slug: 'vases', count: 14 },
  { id: 'incense', name: 'Incense holders', slug: 'incense', count: 22 },
  { id: 'planters', name: 'Planters & pots', slug: 'planters', count: 20 },
  { id: 'kitchen', name: 'Home & kitchen', slug: 'kitchen', count: 22 },
  { id: 'business', name: 'For businesses', slug: 'business', count: 2, highlight: true },
  { id: 'earrings', name: 'Earrings', slug: 'earrings', count: 28 },
];

const AMS_FILAMENT_COLORS: FilamentColor[] = [
  { id: 'black', name: 'Noir Basalte', hex: '#1e2022', inStock: true },
  { id: 'blue', name: 'Majorelle', hex: '#233d99', inStock: true },
  { id: 'gold', name: 'Or Artisanal', hex: '#d49b42', inStock: true },
  { id: 'terracotta', name: 'Terre Cuite', hex: '#b94832', inStock: true },
];

interface CatalogueSidebarProps {
  categories?: CategoryItem[];
  selectedCategory?: string;
  onSelectCategory?: (slug: string) => void;
}

export const CatalogueSidebarCategories: React.FC<CatalogueSidebarProps> = ({
  categories = DEFAULT_CATEGORIES,
  selectedCategory,
  onSelectCategory,
}) => {
  const router = useRouter();
  const searchParams = useSearchParams();
  const currentCategorySlug = selectedCategory ?? (searchParams.get('category') || '');

  const handleCategoryClick = (slug: string) => {
    if (onSelectCategory) {
      onSelectCategory(slug);
      return;
    }
    const params = new URLSearchParams(searchParams.toString());
    if (slug) {
      params.set('category', slug);
    } else {
      params.delete('category');
    }
    params.set('page', '1');
    router.push(`/shop?${params.toString()}`);
  };

  return (
    <aside className="w-full md:w-64 flex-shrink-0 space-y-6">
      {/* Category List Panel */}
      <div className="bg-[#f8f2ee] rounded-2xl p-4 border border-[#dfd9d5] shadow-sm">
        <div className="flex items-center justify-between pb-3 mb-2 border-b border-[#dfd9d5]/60">
          <div className="flex items-center gap-2 font-bold text-[#1e2022] text-sm">
            <svg className="w-4 h-4 text-[#5a5f63]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path strokeLinecap="round" strokeLinejoin="round" strokeWidth="2" d="M4 6h16M4 12h16M4 18h7" />
            </svg>
            <span>Categories</span>
          </div>
          <span className="text-[11px] text-[#5a5f63] font-mono">227 arts</span>
        </div>

        <nav className="space-y-1">
          {categories.map((cat) => {
            const isActive =
              (cat.slug === '' && !currentCategorySlug) ||
              currentCategorySlug === cat.slug;

            return (
              <button
                key={cat.id}
                onClick={() => handleCategoryClick(cat.slug)}
                className={`w-full flex items-center justify-between px-3 py-2 rounded-xl text-xs font-medium transition text-left ${
                  isActive
                    ? 'bg-[#1e2022] text-[#fef8f4] shadow-sm'
                    : cat.highlight
                    ? 'bg-amber-100/70 text-amber-900 hover:bg-amber-100 font-semibold'
                    : 'text-[#414447] hover:bg-white/60 hover:text-[#1e2022]'
                }`}
              >
                <div className="flex items-center gap-2 truncate">
                  {cat.highlight && (
                    <span className="w-2 h-2 rounded-full bg-amber-500 flex-shrink-0" />
                  )}
                  <span className="truncate">{cat.name}</span>
                </div>
                <span
                  className={`text-[10px] font-mono px-1.5 py-0.5 rounded-md ${
                    isActive
                      ? 'bg-white/20 text-white'
                      : 'bg-[#dfd9d5]/50 text-[#5a5f63]'
                  }`}
                >
                  {cat.count}
                </span>
              </button>
            );
          })}
        </nav>
      </div>

      {/* 4-Color AMS Lite Filament Palette Box */}
      <div className="bg-[#f8f2ee] rounded-2xl p-4 border border-[#dfd9d5]">
        <div className="flex items-center justify-between mb-3">
          <span className="text-xs font-bold text-[#1e2022] uppercase tracking-wider">
            AMS 4 Couleurs
          </span>
          <span className="w-2 h-2 rounded-full bg-emerald-500" title="AMS Lite synchronisé" />
        </div>
        <p className="text-[11px] text-[#5a5f63] mb-3 leading-relaxed">
          Filaments PLA+ haute résistance en stock atelier à Casablanca :
        </p>

        <div className="grid grid-cols-2 gap-2 text-[11px]">
          {AMS_FILAMENT_COLORS.map((color) => (
            <div
              key={color.id}
              className="flex items-center gap-2 p-2 rounded-lg bg-white/70 border border-[#dfd9d5]/40"
            >
              <span
                className="w-3.5 h-3.5 rounded-full border border-black/10 flex-shrink-0"
                style={{ backgroundColor: color.hex }}
              />
              <span className="text-[#1e2022] truncate font-medium">{color.name}</span>
            </div>
          ))}
        </div>
      </div>

      {/* Direct Pro Quote / Custom File Banner */}
      <div className="bg-gradient-to-br from-[#1e2022] to-[#2c3034] text-[#fef8f4] rounded-2xl p-4 shadow-sm text-xs">
        <div className="flex items-center gap-2 mb-2 text-amber-300 font-bold">
          <svg className="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path strokeLinecap="round" strokeLinejoin="round" strokeWidth="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
          </svg>
          <span>Besoin d'un volume pro ?</span>
        </div>
        <p className="text-[#dfd9d5] text-[11px] leading-relaxed mb-3">
          Devis express sous 2h pour hôtels, riads, cafés et agences événementielles.
        </p>
        <a
          href="https://wa.me/212661000000?text=Bonjour,%20je%20souhaite%20un%20devis%20de%20volume%20pro"
          target="_blank"
          rel="noopener noreferrer"
          className="block text-center w-full py-2 bg-[#25D366] hover:bg-[#20ba5a] text-white font-bold rounded-lg transition"
        >
          WhatsApp Devis Pro
        </a>
      </div>
    </aside>
  );
};
```

---

## 4. `components/catalogue/CataloguePagination.tsx` (Pagination & Breadcrumbs)

```tsx
'use client';

import React from 'react';
import Link from 'next/link';
import { useRouter, useSearchParams } from 'next/navigation';

interface CataloguePaginationProps {
  currentPage: number;
  totalPages?: number;
  totalItems?: number;
  itemsPerPage?: number;
  onPageChange?: (page: number) => void;
}

export const CataloguePagination: React.FC<CataloguePaginationProps> = ({
  currentPage = 2,
  totalPages = 4,
  totalItems = 48,
  itemsPerPage = 8,
  onPageChange,
}) => {
  const router = useRouter();
  const searchParams = useSearchParams();

  const handlePageSelect = (pageNumber: number) => {
    if (onPageChange) {
      onPageChange(pageNumber);
      return;
    }
    const params = new URLSearchParams(searchParams.toString());
    params.set('page', pageNumber.toString());
    router.push(`/shop?${params.toString()}`);
  };

  const startItem = (currentPage - 1) * itemsPerPage + 1;
  const endItem = Math.min(currentPage * itemsPerPage, totalItems);

  return (
    <div className="w-full flex flex-col md:flex-row items-center justify-between gap-4 py-8 border-t border-[#dfd9d5] mt-10">
      {/* Counters display */}
      <div className="text-xs text-[#5a5f63]">
        Affichage de <span className="font-bold text-[#1e2022]">{startItem}</span> à{' '}
        <span className="font-bold text-[#1e2022]">{endItem}</span> sur{' '}
        <span className="font-bold text-[#1e2022]">{totalItems}</span> créations atelier
      </div>

      {/* Numerical and Arrow Controls */}
      <div className="flex items-center gap-1.5">
        {/* Previous Button */}
        <button
          onClick={() => handlePageSelect(Math.max(1, currentPage - 1))}
          disabled={currentPage <= 1}
          className="px-3 py-2 rounded-lg border border-[#dfd9d5] text-xs font-medium text-[#1e2022] hover:bg-[#f8f2ee] disabled:opacity-30 disabled:pointer-events-none transition flex items-center gap-1"
        >
          <span>←</span>
          <span className="hidden sm:inline">Page précédente</span>
        </button>

        {/* Page Pills (1, 2, 3, 4) */}
        {Array.from({ length: totalPages }, (_, i) => i + 1).map((page) => {
          const isCurrent = page === currentPage;
          return (
            <button
              key={page}
              onClick={() => handlePageSelect(page)}
              className={`w-9 h-9 rounded-lg text-xs font-semibold transition ${
                isCurrent
                  ? 'bg-[#1e2022] text-[#fef8f4] shadow-sm'
                  : 'bg-white border border-[#dfd9d5] text-[#5a5f63] hover:bg-[#f8f2ee] hover:text-[#1e2022]'
              }`}
            >
              {page}
            </button>
          );
        })}

        {/* Next Button */}
        <button
          onClick={() => handlePageSelect(Math.min(totalPages, currentPage + 1))}
          disabled={currentPage >= totalPages}
          className="px-3 py-2 rounded-lg border border-[#dfd9d5] text-xs font-medium text-[#1e2022] hover:bg-[#f8f2ee] disabled:opacity-30 disabled:pointer-events-none transition flex items-center gap-1"
        >
          <span className="hidden sm:inline">Page suivante</span>
          <span>→</span>
        </button>
      </div>

      {/* Jump to Page Quick Select */}
      <div className="flex items-center gap-2 text-xs text-[#5a5f63]">
        <span>Aller à :</span>
        <select
          value={currentPage}
          onChange={(e) => handlePageSelect(Number(e.target.value))}
          className="bg-white border border-[#dfd9d5] rounded-lg px-2 py-1.5 text-xs text-[#1e2022] focus:outline-none focus:ring-1 focus:ring-[#1e2022]"
        >
          {Array.from({ length: totalPages }, (_, i) => i + 1).map((p) => (
            <option key={p} value={p}>
              Page {p}
            </option>
          ))}
        </select>
      </div>
    </div>
  );
};
```

---

## 5. Exemple d'Assemblage Page Next.js (`app/shop/page.tsx`)

```tsx
import React, { Suspense } from 'react';
import { CatalogueNavigation } from '@/components/catalogue/CatalogueNavigation';
import { CatalogueSidebarCategories } from '@/components/catalogue/CatalogueSidebarCategories';
import { CataloguePagination } from '@/components/catalogue/CataloguePagination';

export default async function ShopPage({
  searchParams,
}: {
  searchParams: Promise<{ page?: string; category?: string; q?: string }>;
}) {
  const params = await searchParams;
  const currentPage = Number(params.page) || 1;
  const selectedCategory = params.category || '';

  return (
    <div className="min-h-screen bg-[#fef8f4] text-[#1e2022]">
      {/* Top Header & Search Navigation */}
      <Suspense fallback={<div className="h-28 bg-[#fef8f4]" />}>
        <CatalogueNavigation cartCount={2} cartTotalMad={198} />
      </Suspense>

      {/* Main Container Layout */}
      <main className="max-w-7xl mx-auto px-4 py-8">
        {/* Breadcrumb Banner */}
        <div className="text-xs text-[#5a5f63] mb-6 flex items-center gap-2">
          <a href="/" className="hover:underline">Accueil</a>
          <span>/</span>
          <span className="font-semibold text-[#1e2022]">Boutique & Catalogue 3D</span>
          <span>/</span>
          <span className="text-amber-800">Page {currentPage} sur 4</span>
        </div>

        {/* 2-Column Grid with Left Sidebar */}
        <div className="flex flex-col md:flex-row gap-8 items-start">
          <Suspense fallback={<div className="w-64 h-96 bg-[#f8f2ee] rounded-2xl animate-pulse" />}>
            <CatalogueSidebarCategories selectedCategory={selectedCategory} />
          </Suspense>

          {/* Product Grid Area & Pagination */}
          <div className="flex-1 w-full">
            {/* Products grid injected here */}
            <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
              {/* Cartes produits */}
            </div>

            {/* Pagination Controls */}
            <Suspense fallback={<div className="h-16 w-full animate-pulse" />}>
              <CataloguePagination currentPage={currentPage} totalPages={4} totalItems={48} />
            </Suspense>
          </div>
        </div>
      </main>
    </div>
  );
}
```
