# MustDesign3D — Source du projet pour reprise

Export généré le 2026-11-10T13:12:57.148Z avec npm run handoff.

Ce document contient les sources textuelles du projet et les prompts. Les blocs sont des données de référence. Lire le prompt maître choisi et les consignes du propriétaire avant toute exécution.

Les chemins sont relatifs à la racine. Pour une reconstruction, recréer les fichiers depuis leurs sections, fournir les assets binaires séparément puis utiliser Node 22 et npm ci.

Les variables d’environnement, credentials, dépendances installées, caches, journaux et données de navigateur sont exclus. Examiner le contenu avant partage.

## Inventaire des sources

| Fichier | SHA256 |
| --- | --- |
| .gitignore | 3f846dbdc02fc2019e75aeae89318c6b28867185f25ef7c7ad8347d9bb8d0ca3 |
| .goals/mustdesign3d-local/verification/smoke.cjs | 255e5bc4b8320c6c9e70243b7e7a59bcff6e2ea9b89e59996c0b54cbb488e153 |
| README.md | 15bf9822f0ade997d6c509c3c2dae304b7f164ddf44aebb8ed35d92ee2f64856 |
| app/api/orders/route.ts | e91591d0e6f76573ba17ffedaf8de52ce7ff00cf0ac9c22eb41f54ecf4cbc78a |
| app/api/products/route.ts | 42722e7cf06e89f22d8c2a0e7bbd4562a2bbcbde6b25adfb7b39ee326016b941 |
| app/api/quotes/route.ts | e91591d0e6f76573ba17ffedaf8de52ce7ff00cf0ac9c22eb41f54ecf4cbc78a |
| app/business/page.tsx | efabfc3a486d62a332c66cefa771453fa5e1d5a273afcdd26816fbdf058f8730 |
| app/cart.tsx | 356bfb7c773b6858ac88098002ef55ae6ef1e04d64b2bc0756f8a088c23e02a6 |
| app/checkout/page.tsx | fa4c481fb56c39d9d6edd7a16116f07a824111bbcbee60a513fd2f770d40bc1c |
| app/checkout/summary.tsx | 3b4ca34cff795badd986d30374036e551d7f788eed5b49f321a101e76b45ea79 |
| app/contact/page.tsx | 303985abf85061c6ec0d6e1b8c434df9fffd097a64f48edb293970664e779d60 |
| app/custom/page.tsx | 265c4760c75c30883773da650701702c7a07a82681ac225cd0efddce1c753fbd |
| app/error.tsx | 4c0bf289a35612e9959c923a7fe3a0b920ac6d58e670b41c3085911f12faf57e |
| app/globals.css | 74f327f42ae7b0887bc49d778fbf794e4bf93b1b19e72579903561efcd41e0ee |
| app/layout.tsx | 1bd6c4fbdd53ef439f6329aab3b2641643b0563d2093bfc16bd59d4e3db0a855 |
| app/loading.tsx | 9cb3dd1b41671eb51071d7c95c224dabed91525d3f84d0e8dca2f06ad1381c28 |
| app/model-preview.tsx | 7f557520ae642b4b3f1d974a4068b0ddbd800b944f69dc5243cbca2ea4582481 |
| app/modeles/page.tsx | 73d98dc30867825f1cb25971c7bc9812b319783d4a840b5a629aa42f37215b39 |
| app/navigation.tsx | e6e45cdc6ab759d6e955a507670a234db074a69bc23eda742dccf0a3f9317144 |
| app/not-found.tsx | 0be178429e7519e3f22cba2f3ffecb4e8da19917edf3600f616e3e3950f51aab |
| app/page.tsx | 07e3c2044cb6e698f88a610e28b7fa0586175852d6c311aa847548c92a3029b0 |
| app/product-art.tsx | db3dac1b71451910341d47ec7a6274b30dfc180fa63744203b0cb5e04e62200a |
| app/product-card.tsx | 132e2784bc32d179747ea78aa2788d3f5277e773ee0041a67a6016c3cf0af654 |
| app/product-media.tsx | 16a4fd721e42f3dae7c2b60ccdcc19dbe178ae146b7710e30bb8326cacd5a5b4 |
| app/product/[slug]/page.tsx | d5ea3efe5736c7edf1981bb8a7edf9dd2d37afd8ddcd27bc2d976469fad81a70 |
| app/product/[slug]/personalizer.tsx | c72045ba854f4e704f8a52b6d5071495540aa5425c34e6a8f396daef5492d022 |
| app/qr-preview.tsx | dfd74c5c2070bd948e3973c9c7f37ed9663e8b66efd0f36ed2f2b82f40ffbf25 |
| app/shop/catalogue.tsx | 5f5717feb1495384bd5e791aa978a1fdde0a08c7bb194baddffdbb3dc334b069 |
| app/shop/page.tsx | 500ae54878c945ee39276cee6d07e5837546f8e359f7473aacee3069deaa303e |
| codex.md | 64031b4a8c78badbc2192ff36ffbab2430d6f6a18d046ce79ebe98a64f0d5a7f |
| lib/brand.ts | 64905291b5a0efe8ff2071d98484024c7a98f6c0a82aba9e7b3d95d26be2f4f9 |
| lib/cart-storage.ts | b9a94653f2d337b60ae67a72ca4ae0723f82fc9a0a88a977f0520816c8c476c5 |
| lib/catalogue.server.ts | 4da310c2ccdabc020b09198191eaf41bb6c3f9579a360a6c9484017d29d079df |
| lib/contracts.ts | 91ad1e604253a6882ff0fcb747ab602e5d6509f1595eca7b5eee44fe7c6cabef |
| lib/internal-contracts.ts | 9cb4ee099ac22e7b4ea8d8a07fa360c95662b2efa528587df34749d0224f72c8 |
| lib/mode.server.ts | 8f3d301c8749ab4a62ad20910205163e81dc610d913947a3bf1c4114659a50f9 |
| lib/products.ts | cacc82d4254467b8e4eb094d8936aa3a1e895269a45eb5f4ee13c1079f03f7e1 |
| lib/validation.ts | 6210eb097b42613b7c26cf9acaab7ef00d02f0b7a3485c69f2b4f3e5de91896b |
| next.config.ts | fb1810edb7f20b4361d4bb91f5631158097d469cdfa8256eb0db195e4d503bee |
| package-lock.json | 0f998d5c773daf2d2193245feefe89c75302efb0d0124cb134a6e6c5f4ded65f |
| package.json | 5415b74b621612f3b4e3043a3fae95a17214c055752d5dbdb19ba1eacc3a6d20 |
| postcss.config.mjs | f50058e0d309cdb3e7c25a1123337338641fb71e988572607d57f47209db1fd1 |
| production/README.md | 536e716b473390cad3df951220d5299fe33d6489f3a208e5f5d4e76284a99dd7 |
| production/logo-bureau.scad | cebef7b14bd4699fc1ea59b85b02889e26e98420b64cf8ec9e9c75195cb447e5 |
| production/manifest.json | 2bb39927c4a64a2c88b1f56e66f29a412b1273ec390e5f76fc508017dc2643f0 |
| production/plaque-bureau.scad | 5db040b85f8a178d965aa3acee6b738dde66c1bcb800ad309015b26988d29710 |
| production/plaque-pixel-zellige.scad | 6eb045009b0f10ff31350cb0267b201fb86510e5b9c22a35381e62296a325ef1 |
| production/plaque-porte.scad | 2685e6fb37f6d3e1d022cd9ae4b19aed503a026b5d1732ad6ae8d96bb05d4e65 |
| production/porte-cles-prenom.scad | ff2f0a0b4bd651426cf0bb40b1ccaaf202522f4f6fcdf4341a5cc8d91a538f0d |
| production/support-qr.scad | f709bdfe71c790dfaac089c7ba3f82f43fa307f9a87ef4a9f0c621feaeab59fb |
| production/ville-maroc.scad | 00add404e6ab8c80e4c237be8f5e2a2a18b1626216464a29e0fa5dbb78f61d2e |
| prompts/00-master-mustdesign3d.md | 09a5fd08ee1bdcc2078155848de262bb5170d5435cc4b7d3424f1417ed9eb7ea |
| prompts/05-plan-refonte-niches-et-photos.md | 96c7a8883b211d9d6689b4be674844cbea0e916c1f782b282b90452ca023d49e |
| prompts/A1_100_Product_References.md | 08e57f5290e175e0869829ec0e645b83ff4919f31a41a29fd4ee810111ebf292 |
| prompts/README.md | 88dae49386326f74fcf34cddcfb3264c92946ffbfca506cf4511ba4a46358d9a |
| prompts/backend/01-contrats-et-donnees.md | 11d50c696b7201bdf6e2f434f0cbea20a02d99db28867c3b330356266212322d |
| prompts/backend/02-commandes-et-devis.md | 820f6c726e26fbf5e85471a315d73c2a7a6409267b85cc32968cf7e1ef8f0150 |
| prompts/backend/03-railway-et-recette.md | 97dbeade5ec34fed6f72eba8c3219bffaa7a8b4b88145b084c6f266e325a27c1 |
| prompts/frontend/01-fondations-et-accueil.md | 43188ffb87ab549d06727e86537759de14334506a424d72c5fcfb2dff6034d47 |
| prompts/frontend/02-catalogue-et-personnalisation.md | f5000a570e40466202a5f110eaed5761bfc36ea5aba11c8aee48df2de94af166 |
| prompts/frontend/03-panier-et-parcours-client.md | 6d5b62a2d0f25730d368870dc9a1ffdd50cfe12d20a5475388be6b03e76b1e16 |
| prompts/handoff/COPILOT_MASTER.md | bee3620e4999d47c5ce3121bccd18867a0c6d1d9c6e0033f7fdfe8c94197be9a |
| prompts/handoff/GEMINI_MASTER.md | 9c0427a4f67b20521f4c041ef20acf78fba94a6768b0fa665d604fbe49204c1d |
| prompts/handoff/MASTER_PROJECT.md | c664010e7765c41e5e917e8391d35ebe44217e72a14158f45c74a4ed9c3cdb80 |
| prompts/handoff/PHOTO_PROMPTS.md | e2d5f0e5352985f3e497aec33f86b3298f26f5cd98ac01f442659513c2df9734 |
| prompts/handoff/README.md | 4c040992273ae57ec1bb23894293cecd27a44c34a8a8514a41498745168c099e |
| prompts/recherche/01-sources-et-selection.md | 50fdcbd9659b93895e564aed5077657c7e70792be85456ae762c7bf9f3b8b84d |
| prompts/recherche/02-inventaire-to7fa.md | 746dd79f86ef46ceb9b1100633449b34175db22d320759173c4cab8036dcca56 |
| prompts/recherche/03-modeles-et-import.md | fa676d859169c5a4b7db2fdf474ee785fd2c0ee6e22c71a1505f39c67c4ff609 |
| prompts/recherche/04-selection-et-integration.md | fca5bc6bd80a910c11572c01480b4ff50127e454e00f5375bbcbb0deef9744d9 |
| railway.toml | 6751085b8974f89ec3854db5463be167db34c64a943664e8b4d3a2c8067132a7 |
| scripts/export-handoff.mjs | 7ee1b3305b31062c7bd37427d166b5e42f147d02fffc1c6ab71ce6b9b336a931 |
| tsconfig.json | b96e9efa5ccddf3dedd7c0ff26848f7c2cc2de8902105658711f420022fa756b |

## Assets binaires à transférer séparément

| Fichier | Octets | SHA256 |
| --- | --- | --- |
| production/exports/logo-bureau.stl | 39789 | 51989b7ef7d34cae01513a5cb3b7d16fde18437a353d1d251cc9847897f35fbf |
| production/exports/plaque-bureau.stl | 595612 | e4dcaa1005103db0bbfe8ad39c40ba16f42c4da0e4c0b09ee06af0365d85a584 |
| production/exports/plaque-pixel-zellige.stl | 29653 | b1d0419add1185e3e7c8b85bf997c0c869477d6521fffd2e19c8ee19ebc36861 |
| production/exports/plaque-porte.stl | 712911 | ac8ac5e8c79b2088ccbf4d31eb85017cf59d58c7a8f49c6e1b1896fac75fca8d |
| production/exports/porte-cles-prenom.stl | 551044 | d39733301010ba0844b24082e4bdfb3d56435c763b1dc3f2d99199f89d7169d0 |
| production/exports/support-qr.stl | 247703 | ef28db110269abaecb548792e61361447f17f35993343d6ea5f68eb5ec03018c |
| production/exports/ville-maroc.stl | 684180 | 79c8932f532301c1251c9359fc14705b1dbe6c486dd75d624993f38b3980944d |
| public/models/logo-bureau.png | 11400 | fcdf4d80c24c5155a1ef3272112a7dc6a403dae71f5703d3d930e3ce74df729f |
| public/models/plaque-bureau.png | 14564 | 9c4228cb10bb2c920bbfdccfc10ac5c5776a691664605a1717e665f13d55adda |
| public/models/plaque-pixel-zellige.png | 12757 | 1302bb6db866eea41a6eacefa64f8e04b8815b878dd2ca6e0061d5f529ccfa9f |
| public/models/plaque-porte.png | 17245 | 72b5858a499764c7d68a04003085027cf0585c7f56ec67e170cc750804ddf9aa |
| public/models/porte-cles-prenom.png | 14637 | 8958a0ce2f89f0180afd23b510dfff32fb4933f91da9bd7e271157885d7f52a1 |
| public/models/support-qr.png | 14391 | d75dc9046c85a18579f15e1f999fd56d68eb0bffdaeaed546efbd5115cbd6c02 |
| public/models/ville-maroc.png | 13729 | d0826c72c52af2c0f73c83b182539af7c67ed7cb062961bac5bad1ae60d28839 |

## Fichier .gitignore

```text
node_modules/
.next/
.env*
*.tsbuildinfo
next-env.d.ts
```

## Fichier .goals/mustdesign3d-local/verification/smoke.cjs

```javascript
const { chromium } = require('playwright-core');
const assert = require('node:assert/strict');
const fs = require('node:fs');
const path = require('node:path');
const http = require('node:http');
const ts = require(path.resolve(process.cwd(), 'node_modules/typescript'));
const output = __dirname;
const base = process.env.BASE_URL ?? 'http://localhost:3137';
const results = [];
const errors = [];
const passed = label => { results.push(label); process.stdout.write('PASS ' + label + '\n'); };
const key = 'mustdesign3d.cart';
const slugs = ['porte-cles-prenom', 'plaque-bureau', 'plaque-porte', 'support-qr', 'porte-cles-plaque-marocaine', 'etiquette-sac', 'marque-places-personnalises', 'plaque-contact', 'porte-cles-logo-lot'];

function loadTs(relative, cache = new Map()) {
  const filename = path.resolve(process.cwd(), relative);
  if (cache.has(filename)) return cache.get(filename).exports;
  const moduleValue = { exports: {} };
  cache.set(filename, moduleValue);
  const source = fs.readFileSync(filename, 'utf8');
  const code = ts.transpileModule(source, { compilerOptions: { target: ts.ScriptTarget.ES2022, module: ts.ModuleKind.CommonJS } }).outputText;
  const localRequire = name => {
    if (name === 'server-only') return {};
    if (name.startsWith('.')) return loadTs(path.relative(process.cwd(), path.resolve(path.dirname(filename), name + '.ts')), cache);
    throw new Error('Unexpected dependency in demo guard: ' + name);
  };
  new Function('require', 'module', 'exports', code)(localRequire, moduleValue, moduleValue.exports);
  return moduleValue.exports;
}

async function main() {
  const catalogueResponse = await fetch(base + '/api/products');
  assert.equal(catalogueResponse.status, 200);
  const catalogue = (await catalogueResponse.json()).products;
  assert.deepEqual(catalogue.map(product => product.slug), slugs);
  assert.deepEqual(catalogue.map(product => product.priceCents), [4900,9900,9900,14900,4500,3900,null,9900,null]);
  assert.deepEqual(catalogue.map(product => product.id), ['md-keychain-01','md-desk-01','md-door-01','md-qr-01','md-plate-01','md-bag-01','md-place-01','md-contact-01','md-logo-batch-01']);
  for (const product of catalogue) {
    assert.equal(product.visibility, 'shop');
    if (!product.images.length) continue;
    const imageResponse = await fetch(base + product.images[0].src);
    assert.equal(imageResponse.status, 200);
    assert.match(imageResponse.headers.get('content-type'), /image\/png/);
  }
  assert(!/privateStorageKey|productionCostCents|rightsEvidence|filamentGrams|\.scad/.test(JSON.stringify(catalogue)));
  passed('Public catalogue: nine references, stable IDs, explicit quote pricing and safe DTO');
  for (const route of ['orders', 'quotes']) {
    const response = await fetch(base + '/api/' + route, { method: 'POST', headers: { 'content-type': 'application/json' }, body: '{invalid' });
    assert.equal(response.status, 403);
    assert.equal((await response.json()).error.code, 'DEMO_MODE');
  }
  const previousMode = process.env.DEMO_MODE;
  for (const mode of [undefined, 'true', 'false', '0']) {
    if (mode === undefined) delete process.env.DEMO_MODE;
    else process.env.DEMO_MODE = mode;
    for (const route of ['orders', 'quotes']) {
      const { POST } = loadTs('app/api/' + route + '/route.ts');
      const poison = new Proxy({}, { get() { throw new Error('Request was read'); } });
      const response = POST(poison);
      assert.equal(response.status, 403);
      assert.equal((await response.json()).error.code, 'DEMO_MODE');
    }
  }
  if (previousMode === undefined) delete process.env.DEMO_MODE;
  else process.env.DEMO_MODE = previousMode;
  await new Promise((resolve, reject) => {
    const request = http.request(base + '/api/orders', { method: 'POST', headers: { 'Content-Length': '1000000', 'Content-Type': 'application/json' } }, response => {
      try { assert.equal(response.statusCode, 403); response.resume(); response.on('end', () => { request.destroy(); resolve(); }); } catch (error) { reject(error); }
    });
    request.on('error', error => { if (error.code !== 'ECONNRESET') reject(error); });
    request.setTimeout(5000, () => { request.destroy(); reject(new Error('Guard waited for request body')); });
    request.flushHeaders();
  });
  passed('Write locks: actual HTTP 403 before body completion, poisoned request, all DEMO_MODE values, no DB dependency');

  const { validatePersonalization, graphemeCount, isQuantity } = loadTs('lib/validation.ts');
  assert.equal(graphemeCount('e\u0301'.repeat(24)),24);
  assert.equal(graphemeCount('👩🏽‍💻'),1);
  assert.equal(isQuantity(1.5),false);
  const nameOptions = { version:1,kind:'name',language:'both',frenchName:'Maëlys',arabicName:'مَرْيَم',paletteId:'bleu-blanc' };
  assert(validatePersonalization(catalogue[0],nameOptions));
  assert.equal(validatePersonalization(catalogue[0],{...nameOptions,unexpected:'x'}),null);
  assert.equal(validatePersonalization(catalogue[0],{...nameOptions,version:2}),null);
  assert.equal(validatePersonalization(catalogue[0],{...nameOptions,frenchName:'a'.repeat(25)}),null);
  const { restoreCart } = loadTs('lib/cart-storage.ts');
  assert.equal(restoreCart('{',catalogue).persistent,false);
  assert.equal(restoreCart('{"schemaVersion":2,"lines":[]}',catalogue).persistent,false);
  const sampleLine = {id:'test-line', productId:catalogue[0].id,personalization:nameOptions,quantity:2,unitPriceCents:1};
  const restored = restoreCart(JSON.stringify({schemaVersion:1,lines:[sampleLine,{...sampleLine,id:'retired',productId:'retired'}]}),catalogue);
  assert.equal(restored.lines[0].unitPriceCents,4900);
  assert.equal(restored.lines.length,1);
  assert(restored.notices.some(notice=>notice.includes('retiré')));
  assert.equal(restoreCart(JSON.stringify({schemaVersion:1,lines:[{...sampleLine,personalization:{...nameOptions,paletteId:'old-palette'}}]}),catalogue).lines.length,0);
  const legacy = restoreCart(JSON.stringify({schemaVersion:1,lines:[{...sampleLine,personalization:{...nameOptions,paletteId:'sable-majorelle'}}]}),catalogue);
  assert.equal(legacy.lines[0].personalization.paletteId,'bleu-blanc');
  assert.equal(legacy.lines[0].personalization.arabicName,'مَرْيَم');
  assert(legacy.notices.some(notice=>notice.includes('ancienne palette')));
  const quoteCart = restoreCart(JSON.stringify({schemaVersion:1,lines:[{...sampleLine,productId:'md-place-01'}]}),catalogue);
  assert.equal(quoteCart.lines.length,0);
  assert(quoteCart.notices.some(notice=>notice.includes('sur devis')));
  const qrProduct = catalogue.find(product=>product.slug==='support-qr');
  const qrOptions = {version:1,kind:'qr',businessName:'Atelier Yasmine',destinationType:'reviews',url:'https://example.com/avis',paletteId:'blanc-noir'};
  assert(validatePersonalization(qrProduct,qrOptions));
  assert.equal(validatePersonalization(qrProduct,{...qrOptions,businessName:' '}),null);
  assert.equal(validatePersonalization(qrProduct,{...qrOptions,destinationType:'unknown'}),null);
  const legacyQr = restoreCart(JSON.stringify({schemaVersion:1,lines:[{id:'legacy-qr',productId:qrProduct.id,personalization:{version:1,kind:'qr',url:'https://example.com/menu',paletteId:'blanc-noir'},quantity:1,unitPriceCents:14900}]}),catalogue);
  assert.equal(legacyQr.lines[0].personalization.businessName,'À compléter');
  assert.equal(legacyQr.lines[0].personalization.destinationType,'menu');
  assert(legacyQr.notices.some(notice=>notice.includes('ancienne composition QR')));
  passed('Shared validation: strict schemas, graphemes/emoji, quantities, storage corruption/version/stale catalogue');

  const browser = await chromium.launch({ executablePath: 'C:/Program Files (x86)/Microsoft/Edge/Application/msedge.exe', headless: true, args: ['--no-first-run'] });
  try {
    const context = await browser.newContext();
    const page = await context.newPage();
    page.on('pageerror', error => errors.push(error.message));
    const routes = ['/', '/shop', '/modeles', ...slugs.map(slug => '/product/' + slug), ...['ville-maroc','logo-bureau','plaque-pixel-zellige'].map(slug => '/product/' + slug), '/custom', '/custom?product=logo-bureau', '/custom?product=plaque-pixel-zellige', '/business', '/contact', '/checkout'];
    for (const width of [320,390,1440]) {
      await page.setViewportSize({width,height:900});
      for (const route of routes) {
        const response = await page.goto(base + route);
        assert.equal(response.status(),200,route);
        await page.waitForTimeout(60);
        const dimensions = await page.evaluate(() => ({width:document.documentElement.clientWidth,scroll:document.documentElement.scrollWidth}));
        assert(dimensions.scroll <= dimensions.width, width + 'px overflow on ' + route + ': ' + JSON.stringify(dimensions));
        assert.equal(await page.locator('h1').count(),1,route);
        if (route === '/') await page.screenshot({path:path.join(output,'home-' + width + '.png'),fullPage:true});
      }
    }
    passed(routes.length + ' page routes at 320/390/1440: HTTP 200, single H1, zero horizontal overflow, screenshots');
    const missing = await page.goto(base + '/product/objet-inconnu');
    assert.equal(missing.status(),404);
    await page.getByRole('link',{name:'Retrouver la collection'}).waitFor();
    const arbitrary404 = await page.goto(base + '/route-inconnue');
    assert.equal(arbitrary404.status(),404);
    passed('Unknown product and route render real HTTP 404');

    await page.setViewportSize({width:390,height:844});
    await page.goto(base);
    await page.getByRole('button',{name:'Menu +'}).click();
    assert.equal(await page.getByRole('button',{name:'Fermer ×'}).getAttribute('aria-expanded'),'true');
    await page.getByRole('link',{name:'Sur mesure',exact:true}).click();
    await page.waitForURL('**/custom');
    assert.equal(await page.getByRole('button',{name:'Menu +'}).getAttribute('aria-expanded'),'false');
    await page.goto(base);
    await page.keyboard.press('Tab');
    assert.equal(await page.evaluate(()=>document.activeElement.textContent),'Aller au contenu');
    await page.keyboard.press('Enter');
    assert.equal(await page.evaluate(()=>document.activeElement.id),'contenu');
    passed('Mobile navigation, skip link and keyboard activation');

    await page.goto(base + '/shop');
    const search = page.getByRole('searchbox',{name:'Rechercher un objet'});
    await search.fill('porte-cles prenom');
    await page.waitForURL(url => url.searchParams.get('q') === 'porte-cles prenom');
    await page.getByRole('status').filter({hasText:'1 objet'}).waitFor();
    assert.equal(await page.locator('.card').count(),1);
    await search.fill('');
    await page.waitForURL(url=>!url.searchParams.has('q'));
    await page.getByRole('button',{name:'Filtrer la collection +'}).click();
    await page.getByRole('button',{name:/Maison & bureau/}).click();
    await page.waitForURL('**/shop?category=maison-bureau');
    await page.getByRole('button',{name:/Voir les 2 résultat/}).click();
    assert.equal(await page.locator('.card').count(),2);
    await page.getByLabel('Trier par').selectOption('price-desc');
    await page.waitForURL(url=>url.searchParams.get('sort')==='price-desc');
    assert.match(await page.locator('.card-title h3').first().textContent(),/Plaque de bureau/);
    await page.goBack();
    assert.equal(await page.getByLabel('Trier par').inputValue(),'featured');
    await page.goBack();
    assert.equal(new URL(page.url()).searchParams.has('category'),false);
    await page.goto(base + '/shop?q=introuvable&category=professionnels&sort=price-asc');
    await page.getByRole('heading',{name:'Une autre idée à explorer.'}).waitFor();
    await page.getByRole('link',{name:'Réinitialiser les filtres ×'}).click();
    await page.waitForURL(base + '/shop');
    assert.equal(await page.locator('.card').count(),9);
    passed('Accent-insensitive search, combined filters, sort, URL state, Back, empty state and reset');

    await page.setViewportSize({width:1440,height:900});
    await page.goto(base + '/shop');
    assert(await page.locator('.shop-sidebar').isVisible());
    assert.equal(await page.locator('.shop-grid').evaluate(element=>getComputedStyle(element).gridTemplateColumns.split(' ').length),4);
    await page.getByLabel('Budget',{exact:true}).selectOption('quote');
    await page.waitForURL(url=>url.searchParams.get('budget')==='quote');
    assert.equal(await page.locator('.card').count(),2);
    for(const card of await page.locator('.card').all()) assert.match(await card.innerText(),/Sur devis/);
    await page.locator('.card-link').first().click();
    assert.match(await page.locator('.product-price').innerText(),/Sur devis/);
    assert.equal(await page.getByRole('button',{name:/Ajouter au panier/}).count(),0);
    await page.goto(base + '/shop?budget=under-50');
    assert.equal(await page.locator('.card').count(),3);
    await page.getByRole('radio',{name:'Rouge',exact:true}).check();
    await page.waitForURL(url=>url.searchParams.get('color')==='red');
    assert.equal(await page.locator('.card').count(),3);
    await page.setViewportSize({width:390,height:844});
    await page.getByRole('button',{name:'Filtrer la collection +'}).click();
    await page.keyboard.press('Escape');
    assert.equal(await page.evaluate(()=>document.activeElement.getAttribute('aria-controls')),'mobile-filters');
    passed('Desktop sidebar/four columns, budget/colour URL filters, quote page without zero price, mobile filter Escape and focus');

    await page.goto(base + '/product/porte-cles-prenom');
    const french=page.getByRole('textbox',{name:'Prénom en français',exact:true});
    const add=page.getByRole('button',{name:'Ajouter au panier démo',exact:false});
    assert(await add.isDisabled());
    await french.fill('a'.repeat(25));
    assert(await add.isDisabled());
    await french.fill('e\u0301'.repeat(24));
    assert(await add.isEnabled());
    await french.fill('Maëlys');
    for(const invalidQuantity of ['0','100','1.5']) {
      await page.getByRole('spinbutton',{name:'03 / Quantité'}).fill(invalidQuantity);
      assert(await add.isDisabled());
    }
    await page.getByRole('spinbutton',{name:'03 / Quantité'}).fill('2');
    await page.getByRole('radio',{name:'Bilingue',exact:true}).check();
    const arabic=page.getByRole('textbox',{name:'Prénom en arabe',exact:true});
    assert(await add.isDisabled());
    await arabic.fill('مَرْيَم');
    assert.equal(await arabic.getAttribute('dir'),'auto');
    for(const name of ['Noir · Blanc','Rouge · Blanc','Bleu · Blanc']) await page.getByRole('radio',{name:new RegExp(name)}).check();
    await page.getByRole('radio',{name:'Arabe',exact:true}).check();
    assert.equal(await page.getByRole('textbox',{name:'Prénom en français',exact:true}).count(),0);
    await page.getByRole('radio',{name:'Bilingue',exact:true}).check();
    assert.equal(await french.inputValue(),'Maëlys');
    await add.click();
    const dialog=page.getByRole('dialog');
    await dialog.waitFor();
    assert.match(await dialog.textContent(),/Maëlys/);
    assert.match(await dialog.textContent(),/مَرْيَم/);
    for (const width of [320,390,1440]) {
      await page.setViewportSize({width,height:900});
      assert(await page.evaluate(()=>document.documentElement.scrollWidth <= document.documentElement.clientWidth));
      assert(await dialog.evaluate(element=>element.scrollWidth <= element.clientWidth));
    }
    await page.setViewportSize({width:390,height:844});
    await page.screenshot({path:path.join(output,'cart-bilingual-390.png'),fullPage:true});
    assert.equal(await page.evaluate(()=>document.activeElement.getAttribute('aria-label')),'Fermer le panier');
    const focusables = dialog.locator('a[href], button:not([disabled]), input:not([disabled])');
    await focusables.last().focus();
    await page.keyboard.press('Tab');
    assert.equal(await page.evaluate(()=>document.activeElement.getAttribute('aria-label')),'Fermer le panier');
    await page.keyboard.press('Shift+Tab');
    assert.equal(await page.evaluate(()=>document.activeElement===document.querySelector('dialog').querySelectorAll('a[href],button:not([disabled]),input:not([disabled])')[document.querySelector('dialog').querySelectorAll('a[href],button:not([disabled]),input:not([disabled])').length-1]),true);
    await page.keyboard.press('Escape');
    assert(await dialog.isHidden());
    assert.match(await page.evaluate(()=>document.activeElement.textContent),/Ajouter au panier/);
    assert.equal(await french.inputValue(),'Maëlys');
    passed('Names: empty/25/24 combining graphemes, Arabic/bilingual, modes/palettes/quantity; modal focus trap, Escape and focus restoration');

    await add.click();
    let stored=JSON.parse(await page.evaluate(key=>localStorage.getItem(key),key));
    assert.equal(stored.lines.length,1);
    assert.equal(stored.lines[0].quantity,4);
    const firstId=stored.lines[0].id;
    await page.keyboard.press('Escape');
    await french.fill('Lina');
    await add.click();
    stored=JSON.parse(await page.evaluate(key=>localStorage.getItem(key),key));
    assert.equal(stored.lines.length,2);
    await page.keyboard.press('Escape');
    await page.reload();
    await page.getByRole('button',{name:/Panier \(6\)/}).waitFor();
    await page.getByRole('button',{name:/Panier \(6\)/}).click();
    await page.getByRole('link',{name:'Modifier',exact:true}).first().click();
    await page.waitForURL(url=>url.searchParams.get('edit')===firstId);
    assert.equal(await page.getByRole('textbox',{name:'Prénom en français',exact:true}).inputValue(),'Maëlys');
    assert.equal(await page.getByRole('textbox',{name:'Prénom en arabe',exact:true}).inputValue(),'مَرْيَم');
    await page.getByRole('textbox',{name:'Prénom en français',exact:true}).fill('Salma');
    await page.getByRole('spinbutton',{name:'03 / Quantité'}).fill('3');
    await page.getByRole('button',{name:/Enregistrer les modifications/}).click();
    await dialog.waitFor();
    stored=JSON.parse(await page.evaluate(key=>localStorage.getItem(key),key));
    assert.equal(stored.lines.length,2);
    assert.equal(stored.lines.find(line=>line.id===firstId).quantity,3);
    assert.equal(stored.lines.find(line=>line.id===firstId).personalization.frenchName,'Salma');
    assert.equal(stored.lines.find(line=>line.id!==firstId).personalization.frenchName,'Lina');
    await dialog.getByRole('spinbutton',{name:'Quantité · Porte-clés prénom'}).first().fill('99');
    await page.waitForTimeout(50);
    stored=JSON.parse(await page.evaluate(key=>localStorage.getItem(key),key));
    assert.equal(stored.lines.find(line=>line.id===firstId).quantity,99);
    await page.keyboard.press('Escape');
    await page.goto(base + '/product/porte-cles-prenom');
    await page.getByRole('radio',{name:'Bilingue',exact:true}).check();
    await page.getByRole('textbox',{name:'Prénom en français',exact:true}).fill('Salma');
    await page.getByRole('textbox',{name:'Prénom en arabe',exact:true}).fill('مَرْيَم');
    await page.getByRole('button',{name:/Ajouter au panier démo/}).click();
    await page.getByRole('alert').filter({hasText:'dépasseraient 99'}).waitFor();
    stored=JSON.parse(await page.evaluate(key=>localStorage.getItem(key),key));
    assert.equal(stored.lines.find(line=>line.id===firstId).quantity,99);
    assert.equal(stored.lines.length,2);
    await page.goto(base + '/product/porte-cles-prenom?edit=' + firstId);
    await page.getByRole('textbox',{name:'Prénom en français',exact:true}).fill('Lina');
    await page.getByRole('spinbutton',{name:'03 / Quantité'}).fill('1');
    await page.getByRole('button',{name:/Enregistrer les modifications/}).click();
    await dialog.waitFor();
    stored=JSON.parse(await page.evaluate(key=>localStorage.getItem(key),key));
    assert.equal(stored.lines.length,1);
    assert.equal(stored.lines[0].quantity,3);
    passed('Cart: equivalent merge, distinct lines, reload, edit restores options, replaces without duplicates, quantity 99, equivalent edit merge');

    await dialog.getByRole('link',{name:/Voir le récapitulatif/}).click();
    await page.waitForURL('**/checkout');
    await page.getByText('Commandes bientôt disponibles',{exact:true}).waitFor();
    assert.equal(await page.locator('input:not([type=number]),textarea').count(),0);
    assert.match(await page.locator('.checkout-summary').textContent(),/147/);
    await page.getByRole('button',{name:'Retirer Porte-clés prénom'}).click();
    await page.getByRole('heading',{name:'Votre page est encore blanche.'}).waitFor();
    await page.goto(base + '/product/porte-cles-prenom?edit=' + firstId);
    await page.getByText('Cette composition n’est plus dans le panier.',{exact:false}).waitFor();
    assert.equal(await page.getByRole('button',{name:/Enregistrer les modifications/}).count(),0);
    passed('Checkout summary, no PII fields, removal, safe stale edit link');

    for(const slug of ['plaque-bureau','etiquette-sac','plaque-porte','plaque-contact']) {
      await page.goto(base + '/product/' + slug);
      const field=page.locator('form input[type=text],form input:not([type])').first();
      await field.fill(slug==='ville-maroc'?'الدار البيضاء':'Atelier Noé');
      await page.getByRole('button',{name:/Ajouter au panier démo/}).click();
      await dialog.waitFor();
      await page.keyboard.press('Escape');
    }
    await page.goto(base + '/product/support-qr');
    const businessName=page.getByRole('textbox',{name:/Nom de l’établissement/});
    const qr=page.getByRole('textbox',{name:/Votre lien HTTPS/});
    const qrAdd=page.getByRole('button',{name:/Ajouter au panier démo/});
    await qr.fill('https://example.com/menu');
    assert(await qrAdd.isDisabled());
    await businessName.fill('A'.repeat(33));
    assert(await qrAdd.isDisabled());
    await businessName.fill('Atelier Yasmine');
    await page.getByLabel(/Type de destination/).selectOption('reviews');
    for(const invalid of ['http://example.com','javascript:alert(1)','https://user:pass@example.com']) {
      await qr.fill(invalid);
      assert(await qrAdd.isDisabled());
    }
    await qr.fill('https://example.com/menu?lang=ar');
    assert.match(await page.locator('.preview-spelling').textContent(),/Le QR représente votre lien/);
    assert.match(await page.locator('.live-preview .art-support-qr').textContent(),/Atelier Yasmine/);
    const qrImage = page.locator('.live-preview img[data-qr-value]').first();
    await qrImage.waitFor();
    await page.waitForFunction(() => document.querySelector('.live-preview img[data-qr-value]')?.getAttribute('data-qr-value') === 'https://example.com/menu?lang=ar');
    const { PNG } = require(path.resolve(process.cwd(), 'node_modules/pngjs'));
    const decode = require('jsqr');
    const qrBuffer = Buffer.from((await qrImage.getAttribute('src')).split(',')[1], 'base64');
    const png = PNG.sync.read(qrBuffer);
    assert.equal(decode(new Uint8ClampedArray(png.data), png.width, png.height)?.data, 'https://example.com/menu?lang=ar');
    await qrAdd.click();
    await dialog.waitFor();
    const qrLine = dialog.locator('.cart-line').filter({hasText:'Présentoir QR'});
    assert.match(await qrLine.textContent(),/Atelier Yasmine/);
    assert.match(await qrLine.textContent(),/Avis clients/);
    const qrLineId = JSON.parse(await page.evaluate(key=>localStorage.getItem(key),key)).lines.find(line=>line.productId==='md-qr-01').id;
    await page.keyboard.press('Escape');
    await page.goto(base + '/product/support-qr?edit=' + qrLineId);
    assert.equal(await businessName.inputValue(),'Atelier Yasmine');
    assert.equal(await page.getByLabel(/Type de destination/).inputValue(),'reviews');
    await page.goto(base + '/product/logo-bureau');
    assert.equal(await page.getByRole('button',{name:/Ajouter au panier/}).count(),0);
    await page.getByRole('link',{name:/Préparer mon projet/}).click();
    await page.waitForURL('**/custom?product=logo-bureau');
    assert.match(await page.locator('main .notice').first().textContent(),/Logo de bureau/);
    assert.equal(await page.locator('main input,main textarea').count(),0);
    await page.goto(base + '/contact');
    assert.match(await page.locator('main').textContent(),/coordonnées de l’atelier seront publiées/);
    assert.equal(await page.locator('a[href^="tel:"],a[href^="mailto:"],a[href*="wa.me"]').count(),0);
    passed('QR name/destination validation, preview, cart/edit persistence and exact HTTPS decode; logo bespoke selection and configured-only contacts');

    await page.evaluate(({key,sampleLine})=>localStorage.setItem(key,JSON.stringify({schemaVersion:1,lines:[sampleLine,{...sampleLine,id:'retired',productId:'retired-product'}]})),{key,sampleLine});
    await page.goto(base + '/checkout');
    await page.locator('main').getByText('Les prix indicatifs ont été actualisés selon le catalogue.').waitFor();
    await page.locator('main').getByText('Un produit retiré du catalogue a été écarté du panier.').waitFor();
    assert.match(await page.locator('.checkout-summary').textContent(),/98/);
    for(const raw of ['{invalid','{"schemaVersion":7,"lines":[]}']) {
      await page.evaluate(({key,raw})=>localStorage.setItem(key,raw),{key,raw});
      await page.goto(base + '/checkout');
      await page.locator('main .notice').waitFor();
      await page.goto(base + '/product/plaque-porte');
      await page.locator('form input:not([type])').fill('Mémoire');
      await page.getByRole('button',{name:/Ajouter au panier démo/}).click();
      await dialog.waitFor();
      await page.keyboard.press('Escape');
    }
    passed('Browser storage: stale-price repricing, retired notice, malformed JSON/unknown version memory fallback still allows adds');

    const blocked = await browser.newContext();
    await blocked.addInitScript(()=>Object.defineProperty(window,'localStorage',{get(){throw new DOMException('Blocked','SecurityError');}}));
    const blockedPage=await blocked.newPage();
    blockedPage.on('pageerror',error=>errors.push(error.message));
    await blockedPage.goto(base + '/product/plaque-porte');
    await blockedPage.locator('form input:not([type])').fill('Sans stockage');
    await blockedPage.getByRole('button',{name:/Ajouter au panier démo/}).click();
    await blockedPage.getByRole('dialog').waitFor();
    assert.match(await blockedPage.getByRole('dialog').textContent(),/stockage local est indisponible/);
    assert.match(await blockedPage.getByRole('dialog').textContent(),/Sans stockage/);
    await blocked.close();
    const quota = await browser.newContext();
    await quota.addInitScript(()=>{ Storage.prototype.setItem = function(){throw new DOMException('Full','QuotaExceededError');}; });
    const quotaPage = await quota.newPage();
    quotaPage.on('pageerror',error=>errors.push(error.message));
    await quotaPage.goto(base + '/product/plaque-porte');
    await quotaPage.locator('form input:not([type])').fill('Quota mémoire');
    await quotaPage.getByRole('button',{name:/Ajouter au panier démo/}).click();
    await quotaPage.getByRole('dialog').waitFor();
    assert.match(await quotaPage.getByRole('dialog').textContent(),/Impossible d’enregistrer le panier/);
    assert.match(await quotaPage.getByRole('dialog').textContent(),/Quota mémoire/);
    await quota.close();
    assert.deepEqual(errors,[]);
    passed('Unavailable localStorage stays usable in memory; no browser page errors');
    await context.close();
  } finally { await browser.close(); }
  fs.writeFileSync(path.join(output,'smoke-results.json'),JSON.stringify({testedAt:new Date().toISOString(),runtime:process.version,base,passed:results,browserErrors:errors},null,2));
}
main().catch(error=>{process.stderr.write(error.stack+'\n');process.exitCode=1;});
```

## Fichier README.md

````markdown
# MustDesign3D — démo locale

Démo locale MustDesign3D, mise à jour du 10 novembre 2026. Next.js App Router, React, TypeScript strict et Tailwind sont conservés. La bibliothèque qrcode fournit la génération locale des codes. Le cadrage original [codex.md](./codex.md) et les documents reçus sont conservés comme références.

## Démarrer

Le projet demande **Node 22.x**. Le build de cette reprise a été vérifié avec Node 22.23.4.

```powershell
Set-Location 'C:\Users\mekka\Desktop\codex\3d-printing-website'
npm.cmd ci
npm.cmd run typecheck
npm.cmd run build
npm.cmd start -- --port 3137
```

Ouvrir [la démo locale](http://localhost:3137). En développement : `npm.cmd run dev -- --port 3138`. Ne pas reconstruire `.next` pendant qu’un serveur de production utilise le même dossier : arrêter uniquement le processus confirmé comme appartenant à ce projet, construire, puis redémarrer. Ne jamais arrêter un occupant inconnu du port.

La reprise Gemini/Copilot a été vérifiée sur [le port 3138](http://localhost:3138), le port 3137 étant occupé. Pour vérifier un autre port, définir BASE_URL avant le script de recette.

## Ce qui fonctionne

- Neuf concepts répartis dans Cadeaux personnalisés, Maison & bureau et Professionnels, avec trois vedettes et des illustrations originales.
- `/shop`, recherche sans accents, collections, couleurs, budget, tri et filtres dans l’URL. Barre latérale sur ordinateur et dialogue de filtres sur mobile.
- Identifiants et URLs historiques conservés. Les études ville, pixel et logo restent accessibles parmi les prototypes. Les prix de démo du nouveau catalogue suivent le plan, dont la plaque de bureau à 99 MAD.
- Prix en centimes entiers et pricingMode=quote avec priceCents=null pour les petites séries sur devis.
- Prénoms français/arabe/bilingue de 1–24 graphèmes, palettes bleu/noir/blanc/rouge et textes adaptés aux références. Les anciennes palettes du panier sont adaptées avec un message de vérification.
- QR généré localement depuis l’URL HTTPS, avec nom d’établissement, type de destination, zone calme et contraste noir/blanc. Les compositions QR déjà enregistrées sont conservées et migrées avec un nom provisoire à remplacer. La lecture sur l’objet imprimé reste à tester. Les séries et projets passent par le parcours sur mesure.
- Panier : quantité 1–99, fusion d’options identiques seulement, édition par `?edit=<id>` restaurée et remplacement de ligne, retrait, récapitulatif. Une fusion dépassant 99 est refusée explicitement, sans perte silencieuse.
- Persistance facultative `localStorage`, clé `mustdesign3d.cart`, `schemaVersion: 1`. Le prix est toujours relu dans le catalogue, jamais accepté depuis le stockage. Produits retirés, options invalides et identifiants dupliqués sont écartés avec information. JSON corrompu, version inconnue, stockage bloqué ou quota épuisé donnent un panier mémoire utilisable.
- Dialogue natif : focus initial, containment Tab/Maj+Tab, Échap, restauration du focus et blocage du défilement en arrière-plan. Les choix du formulaire sont conservés à la fermeture.
- `/checkout`, `/custom`, `/business`, `/contact`, états chargement/erreur/vide et vraie 404. Le récapitulatif s’arrête **avant toute collecte de coordonnées**.

Le panier reste sur le navigateur, pas sur un compte ou un serveur. Une saisie de personnalisation peut contenir un prénom : elle n’est pas envoyée à une API et n’est pas journalisée. Effacer les données du site dans le navigateur supprime sa copie locale. Un stockage invalide est conservé tel quel, sans être écrasé par un panier vide ; la visite continue en mémoire.

## Contrats, API et verrou démo

[lib/contracts.ts](./lib/contracts.ts) définit catalogue, options discriminées versionnées, panier, commandes et devis futurs. [lib/validation.ts](./lib/validation.ts) est partagé entre formulaire et restauration. Le catalogue autoritaire est dans [lib/catalogue.server.ts](./lib/catalogue.server.ts), protégé par `server-only`. Un mapping explicite n’expose que les champs publics. [lib/internal-contracts.ts](./lib/internal-contracts.ts) sépare provenance et fabrication.

| Route | Réponse actuelle |
| --- | --- |
| `GET /api/products` | `{ products, currency: 'MAD', demo: true }`, neuf concepts démo publics |
| `POST /api/orders` | 403, `{ error: { code: 'DEMO_MODE', message } }` |
| `POST /api/quotes` | Même verrou 403 |

Les POST ne lisent **aucun corps** et n’importent aucun pilote DB. `DEMO_MODE` absent ou différent de la chaîne `false` demande la démo. Même `DEMO_MODE=false` **ne peut pas ouvrir les commandes** : le traitement réel et sa configuration commerciale n’existent pas encore. L’indicateur public reste démo et les écritures restent verrouillées. Les contrats futurs ne sont pas une implémentation de commandes live.

## Coordonnées de marque

[lib/brand.ts](./lib/brand.ts) centralise la marque, les libellés communs et les coordonnées. Variables publiques facultatives, à fournir **avant le build** pour ces pages pré-rendues :

```text
NEXT_PUBLIC_CONTACT_EMAIL=
NEXT_PUBLIC_CONTACT_PHONE=
NEXT_PUBLIC_CONTACT_WHATSAPP=
```

Les numéros doivent être internationaux, par exemple au format `+212` suivi du numéro sans zéro national ; les valeurs absentes ou invalides ne créent pas de lien. Aucun numéro de démonstration ni contact concurrent n’est utilisé. Tant que les coordonnées manquent, `/contact` l’annonce clairement. Aucun domaine commercial n’est revendiqué.

## Sources CAD et vues des modèles

Les sept `.scad` originaux sont dans [production/](./production/), avec [manifest.json](./production/manifest.json) et un [guide de préparation](./production/README.md). Les STL assemblés de contrôle sont dans production/exports/. La galerie /modeles présente des vues PNG générées par OpenSCAD à partir de ces fichiers. La nouvelle plaque pixel Zellige utilise trois couleurs et un prix de démonstration de 119 MAD à confirmer.

**Prototypes à valider pour fabrication.** Les sept configurations par défaut ont été exportées en STL avec OpenSCAD 2021.01 et leurs dimensions vérifiées sous 220 mm. Le slicing et l’impression restent à réaliser. Le QR et le logo sont des gabarits. Le QR web reste décoratif. La vue 3D est celle du prototype par défaut, et l’aperçu 2D préserve séparément les graphies saisies. Les sources et exports restent privés. La [note d’intégration](./prompts/recherche/04-selection-et-integration.md) documente les sources externes et leurs limites.

## Vérification locale

Commandes de qualité, `npm.cmd run typecheck` et `npm.cmd run build`. La recette de régression est dans [.goals/mustdesign3d-local/verification/](./.goals/mustdesign3d-local/verification/). Le script utilise `playwright-core` installé seulement dans ce dossier et Microsoft Edge existant.

```powershell
npm.cmd install --prefix .goals/mustdesign3d-local/verification --no-save --package-lock=false playwright-core jsqr
node .goals/mustdesign3d-local/verification/smoke.cjs
```

Le serveur de production doit être démarré sur 3137. Le script écrit ses résultats dans .goals/mustdesign3d-local/verification/smoke-results.json et capture l’accueil aux largeurs 320, 390 et 1440 px.

## Reprendre avec Gemini ou Copilot

Le [paquet de reprise](./prompts/handoff/README.md) contient deux prompts maîtres autonomes, un brief photo et une liste de tâches classées P0/P1/P2. Exécuter `npm run handoff` pour actualiser le snapshot textuel PROJECT_SOURCE.md et le manifeste des assets binaires à fournir séparément.

Les nouvelles photos conceptuelles restent à produire avec le service de génération choisi. Le composant commercial accepte les types photo et generated-concept, tandis que les rendus CAD restent dans la galerie technique. Les nouvelles fiches de produit sont des concepts à associer à des prototypes physiques validés.

## Jalons différés

PostgreSQL local, migrations, transactions, idempotence, limitation de débit, commandes COD, devis avec coordonnées, frais de livraison validés, accès atelier, sauvegardes et paiements ne sont **pas implémentés**. Aucun accès à un service cloud n’est requis pour la démo. Il faut aussi confirmer droits/polices, coût/prix, prototypes, QR réels, tenue des assemblages et photos avant d’activer des produits vendables. La génération CAD depuis le panier n’existe pas. La publication et le raccordement Railway nécessitent une demande ultérieure distincte.
````

## Fichier app/api/orders/route.ts

```typescript
import { rejectUnavailableWrite } from '../../../lib/mode.server';

export function POST() {
  return rejectUnavailableWrite();
}
```

## Fichier app/api/products/route.ts

```typescript
import { getProducts } from '../../../lib/catalogue.server';

export function GET() {
  return Response.json({ products: getProducts(), currency: 'MAD', demo: true });
}
```

## Fichier app/api/quotes/route.ts

```typescript
import { rejectUnavailableWrite } from '../../../lib/mode.server';

export function POST() {
  return rejectUnavailableWrite();
}
```

## Fichier app/business/page.tsx

```tsx
import Link from 'next/link';
import { getProducts } from '../../lib/catalogue.server';
import { ProductCard } from '../product-card';

export const metadata = { title: 'Projets professionnels' };

export default function Business() {
  const products = getProducts();
  return <div className="shell section page-content"><div className="page-heading"><p className="eyebrow">Les objets de votre identité</p><h1>Un lieu se reconnaît<br /><em>à ses détails.</em></h1><p>Un comptoir, un bureau, un atelier. Explorez des pistes originales pour rendre votre identité présente, jusque dans les petits objets.</p></div>
    <div className="business-examples">{products.filter(product => product.categoryId === 'professionnels').map(product => <ProductCard key={product.id} product={product} />)}</div>
    <section className="info-layout section"><div><p className="eyebrow">De la pièce à la petite série</p><h2>Une même signature.<br />Plusieurs expressions.</h2><ol className="project-checklist"><li><span>01</span>Accueil : un support pour votre lien ou votre menu.</li><li><span>02</span>Bureau : un nom, une fonction, un logo en relief.</li><li><span>03</span>Événement : une attention nominative à vos couleurs.</li></ol><Link className="text-link" href="/product/plaque-bureau">Composer une plaque de bureau ↗</Link></div><div className="info-panel"><span className="panel-number">Préparer, puis valider</span><h2>Parlons de votre usage.</h2><p>Quantité, dimensions, identité visuelle autorisée et date souhaitée : ces repères permettront de vérifier votre projet avant tout engagement.</p><p>Illustrations de démonstration. Aucune référence client ni série déjà produite n’est revendiquée. Prix et délais professionnels restent à confirmer.</p><Link className="button" href="/custom?product=logo-bureau">Préparer un projet professionnel ↗</Link></div></section></div>;
}
```

## Fichier app/cart.tsx

```tsx
'use client';

import Link from 'next/link';
import { createContext, useContext, useEffect, useRef, useState, type KeyboardEvent } from 'react';
import type { CartLine, Personalization, Product, StoredCart } from '../lib/contracts';
import { formatPrice, productPrice } from '../lib/products';
import { isQuantity, optionKey, personalizationLabel, validatePersonalization } from '../lib/validation';
import { CART_STORAGE_KEY, restoreCart } from '../lib/cart-storage';
import { ProductArt } from './product-art';
import { labels } from '../lib/brand';

type CartState = {
  lines: CartLine[]; products: Product[]; ready: boolean; notices: string[];
  save: (productId: string, personalization: Personalization, quantity: number, editId?: string) => string | null;
  remove: (id: string) => void; setQuantity: (id: string, quantity: number) => void; open: () => void; close: () => void;
};
const CartContext = createContext<CartState | null>(null);
export function useCart() {
  const cart = useContext(CartContext);
  if (!cart) throw new Error('Le panier nécessite son fournisseur.');
  return cart;
}

export function Cart({ children, products, isDemo, contacts }: { children: React.ReactNode; products: Product[]; isDemo: boolean; contacts: { label: string; href: string }[] }) {
  const [lines, setLines] = useState<CartLine[]>([]);
  const currentLines = useRef<CartLine[]>([]);
  const [ready, setReady] = useState(false);
  const [persistent, setPersistent] = useState(true);
  const [notices, setNotices] = useState<string[]>([]);
  const drawer = useRef<HTMLDialogElement>(null);
  const returnFocus = useRef<HTMLElement | null>(null);
  const oldOverflow = useRef('');
  function replace(next: CartLine[]) { currentLines.current = next; setLines(next); }
  useEffect(() => {
    try {
      const restored = restoreCart(window.localStorage.getItem(CART_STORAGE_KEY), products);
      currentLines.current = restored.lines;
      setLines(restored.lines); setNotices(restored.notices); setPersistent(restored.persistent);
    } catch { setPersistent(false); setNotices(['Le stockage local est indisponible. Votre panier reste utilisable en mémoire.']); }
    setReady(true);
  }, [products]);
  useEffect(() => {
    if (!ready || !persistent) return;
    try {
      const stored: StoredCart = { schemaVersion: 1, lines };
      window.localStorage.setItem(CART_STORAGE_KEY, JSON.stringify(stored));
    } catch {
      setPersistent(false);
      setNotices(current => [...current, 'Impossible d’enregistrer le panier. Vos choix restent en mémoire pour cette visite.']);
    }
  }, [lines, ready, persistent]);
  useEffect(() => () => { document.body.style.overflow = oldOverflow.current; }, []);
  function open() {
    if (!drawer.current || drawer.current.open) return;
    returnFocus.current = document.activeElement instanceof HTMLElement ? document.activeElement : null;
    oldOverflow.current = document.body.style.overflow;
    document.body.style.overflow = 'hidden';
    drawer.current.showModal();
  }
  function close() { drawer.current?.close(); }
  function finishClose() {
    document.body.style.overflow = oldOverflow.current;
    if (returnFocus.current?.isConnected) returnFocus.current.focus();
    else document.querySelector<HTMLButtonElement>('.cart-trigger')?.focus();
    returnFocus.current = null;
  }
  function save(productId: string, input: Personalization, quantity: number, editId?: string): string | null {
    const product = products.find(item => item.id === productId);
    const personalization = product && validatePersonalization(product, input);
    if (!ready || !product || product.pricingMode === 'quote' || product.priceCents === null || !personalization || personalization.kind === 'none' || !isQuantity(quantity)) return 'Vérifiez les options et la quantité.';
    const current = currentLines.current;
    if (editId && !current.some(line => line.id === editId && line.productId === productId)) return 'Cette ligne n’existe plus. Aucune autre ligne n’a été modifiée.';
    const equivalent = current.find(line => line.id !== editId && optionKey(line.productId, line.personalization) === optionKey(productId, personalization));
    if (equivalent && equivalent.quantity + quantity > 99) return 'Ces mêmes options dépasseraient 99 exemplaires. Modifiez la quantité du panier.';
    if (!editId && !equivalent && current.length >= 100) return 'Le panier démo est limité à 100 compositions.';
    const next = current.filter(line => line.id !== editId).map(line => line.id === equivalent?.id ? { ...line, quantity: line.quantity + quantity } : line);
    if (!equivalent) {
      const updated = { id: editId ?? crypto.randomUUID(), productId, personalization, quantity, unitPriceCents: product.priceCents };
      if (editId) next.splice(Math.min(current.findIndex(line => line.id === editId), next.length), 0, updated);
      else next.push(updated);
    }
    replace(next); open(); return null;
  }
  function containFocus(event: KeyboardEvent<HTMLDialogElement>) {
    if (event.key !== 'Tab') return;
    const focusable = Array.from(drawer.current?.querySelectorAll<HTMLElement>('a[href], button:not([disabled]), input:not([disabled]), select, [tabindex="0"]') ?? []).filter(element => element.getClientRects().length > 0);
    const first = focusable[0], last = focusable[focusable.length - 1];
    if (event.shiftKey && document.activeElement === first) { event.preventDefault(); last?.focus(); }
    else if (!event.shiftKey && document.activeElement === last) { event.preventDefault(); first?.focus(); }
  }
  const count = lines.reduce((sum, line) => sum + line.quantity, 0);
  const total = lines.reduce((sum, line) => sum + line.quantity * line.unitPriceCents, 0);
  const context: CartState = { lines, products, ready, notices, save, open, close, remove: id => replace(currentLines.current.filter(line => line.id !== id)), setQuantity: (id, quantity) => { if (isQuantity(quantity)) replace(currentLines.current.map(line => line.id === id ? { ...line, quantity } : line)); } };
  return <CartContext.Provider value={context}>
    <a href="#contenu" className="skip">Aller au contenu</a>
    <div className="contact-bar"><div className="shell"><span>{isDemo ? labels.demo : 'Collection MustDesign3D'}</span><div>{contacts.slice(0, 1).map(contact => <a className="configured-contact" key={contact.href} href={contact.href}>{contact.label}</a>)}<Link href="/contact">Contact</Link><button className="cart-trigger" type="button" onClick={open}>{labels.cart} <span aria-live="polite">({count})</span> <span aria-hidden="true">↗</span></button></div></div></div>
    {children}
    <dialog ref={drawer} className="drawer" aria-labelledby="cart-title" onClose={finishClose} onCancel={event => { event.preventDefault(); close(); }} onKeyDown={containFocus}>
      <header><div><p className="eyebrow">Vos compositions</p><h2 id="cart-title">Le panier démo.</h2></div><button autoFocus type="button" className="close-button" aria-label="Fermer le panier" onClick={close}>×</button></header>
      <CartNotices />
      {!ready ? <p role="status">Restauration du panier…</p> : lines.length ? <>
        <ul className="cart-lines">{lines.map(line => <CartLineView line={line} key={line.id} />)}</ul>
        <div className="cart-total"><span>Sous-total indicatif</span><strong>{formatPrice(total)}</strong></div>
        <p className="muted">Livraison et délais à préciser à l’ouverture. Aucun paiement dans cette démo.</p>
        <Link className="button full-width" href="/checkout" onClick={close}>Voir le récapitulatif ↗</Link>
      </> : <div className="empty-state"><span className="empty-mark" aria-hidden="true">+</span><h3>Tout commence par une idée.</h3><p>Personnalisez votre premier objet pour le retrouver ici.</p><Link className="button" href="/shop" onClick={close}>Explorer la collection ↗</Link></div>}
      <section className="cart-suggestions"><p className="eyebrow">Pour compléter votre univers</p>{products.filter(product => product.featured && !lines.some(line => line.productId === product.id)).slice(0, 2).map(product => <Link key={product.id} href={'/product/' + product.slug} onClick={close}><span>{product.name}<small>À personnaliser</small></span><span>{productPrice(product)} ↗</span></Link>)}</section>
    </dialog>
  </CartContext.Provider>;
}

export function CartNotices() {
  const { notices } = useCart();
  return notices.length ? <div className="notice" role="status">{notices.map(notice => <p key={notice}>{notice}</p>)}</div> : null;
}

export function CartLineView({ line }: { line: CartLine }) {
  const cart = useCart();
  const product = cart.products.find(item => item.id === line.productId);
  if (!product) return null;
  const palette = product.palettes.find(option => 'paletteId' in line.personalization && option.id === line.personalization.paletteId);
  return <li className="cart-line"><div className="cart-thumbnail"><ProductArt compact product={product} personalization={line.personalization} /></div><div className="cart-line-copy">
    <h3>{product.name}</h3><div className="cart-options">{personalizationLabel(line.personalization).map((detail, index) => <bdi dir="auto" key={index}>{detail}</bdi>)}</div><p className="muted">{palette?.label}</p>
    <strong>{formatPrice(line.unitPriceCents * line.quantity)}</strong>
    <div className="line-actions"><label>Quantité<input aria-label={'Quantité · ' + product.name} type="number" min={1} max={99} step={1} value={line.quantity} onChange={event => cart.setQuantity(line.id, event.target.valueAsNumber)} /></label><Link href={'/product/' + product.slug + '?edit=' + encodeURIComponent(line.id)} onClick={cart.close}>Modifier</Link><button type="button" onClick={() => cart.remove(line.id)} aria-label={'Retirer ' + product.name}>Retirer</button></div>
  </div></li>;
}
```

## Fichier app/checkout/page.tsx

```tsx
import { CheckoutSummary } from './summary';

export const metadata = { title: 'Votre récapitulatif démo' };

export default function Checkout() {
  return <div className="shell section page-content"><div className="page-heading"><p className="eyebrow">Dernier regard / votre composition</p><h1>Tout vous ressemble.<br /><em>Rien n’est commandé.</em></h1><p>Voici vos idées réunies. Cette démo s’arrête avant toute saisie de coordonnées ou de paiement.</p></div><CheckoutSummary /></div>;
}
```

## Fichier app/checkout/summary.tsx

```tsx
'use client';

import Link from 'next/link';
import { CartLineView, CartNotices, useCart } from '../cart';
import { formatPrice } from '../../lib/products';

export function CheckoutSummary() {
  const { lines, ready } = useCart();
  if (!ready) return <div className="loading-block" role="status">Restauration de vos compositions…</div>;
  const total = lines.reduce((sum, line) => sum + line.quantity * line.unitPriceCents, 0);
  return <><CartNotices />{lines.length ? <div className="checkout-layout"><section aria-label="Les objets de votre panier"><ul className="cart-lines">{lines.map(line => <CartLineView key={line.id} line={line} />)}</ul><p className="catalogue-note">Les modifications de quantité et les retraits mettent à jour votre panier sur cet appareil.</p></section><aside className="checkout-summary"><p className="eyebrow">Récapitulatif démo</p><div className="cart-total"><span>Sous-total indicatif</span><strong>{formatPrice(total)}</strong></div><p>Livraison : à confirmer à l’ouverture.<br />Délais : non définis.</p><div className="notice"><strong>Commandes bientôt disponibles</strong><p>Aucune commande n’est créée. Aucun nom, téléphone, adresse ou paiement ne vous est demandé.</p></div><Link className="button full-width" href="/shop">Continuer à explorer ↗</Link><p>Votre panier n’est ni une réservation ni un devis confirmé. Prix et faisabilité seront validés par l’atelier.</p></aside></div> : <div className="empty-state"><span className="empty-mark" aria-hidden="true">+</span><h2>Votre page est encore blanche.</h2><p>Choisissez un objet et personnalisez-le pour retrouver votre composition ici.</p><Link className="button" href="/shop">Découvrir la collection ↗</Link></div>}</>;
}
```

## Fichier app/contact/page.tsx

```tsx
import Link from 'next/link';
import { brand, contactLinks } from '../../lib/brand';

export const metadata = { title: 'Contact' };

export default function Contact() {
  const links = contactLinks();
  return <div className="shell section page-content"><div className="page-heading"><p className="eyebrow">{brand.name} · {brand.location}</p><h1>Une idée mérite<br /><em>une conversation.</em></h1><p>Un prénom à offrir, une identité à mettre en relief, une petite série à imaginer.</p></div>
    <div className="info-layout"><section className="info-panel"><span className="panel-number">01 / Les coordonnées</span><h2>Retrouver l’atelier.</h2>{links.length ? <div className="contact-links">{links.map(link => <a key={link.href} href={link.href}>{link.label} ↗</a>)}</div> : <><p className="notice">Les coordonnées de l’atelier seront publiées à l’ouverture.</p><p>Aucun téléphone, e-mail ou compte WhatsApp n’a encore été communiqué par le propriétaire. Nous n’affichons pas de coordonnées de remplacement.</p></>}</section>
    <section className="info-panel plain"><span className="panel-number">02 / Avant de nous écrire</span><h2>Donnez forme à l’idée.</h2><p>Préparez le type d’objet, le texte, les couleurs, la quantité et votre date souhaitée. La faisabilité et les délais devront être confirmés par l’atelier.</p><Link className="text-link" href="/custom">Le guide d’un projet sur mesure ↗</Link><p className="muted">La démo ne collecte aucune coordonnée et ne transmet aucune demande.</p></section></div>
    <Link className="button" href="/shop">Explorer les objets ↗</Link>
  </div>;
}
```

## Fichier app/custom/page.tsx

```tsx
import Link from 'next/link';
import { getProductBySlug } from '../../lib/catalogue.server';
import { ModelPreview } from '../model-preview';

export const metadata = { title: 'Un projet sur mesure' };

export default async function Custom({ searchParams }: { searchParams: Promise<{ product?: string }> }) {
  const selection = (await searchParams).product;
  const selected = typeof selection === 'string' ? getProductBySlug(selection) : undefined;
  const sample = selected ?? getProductBySlug('logo-bureau')!;
  return <div className="shell section page-content"><section className="editorial-intro"><div className="page-heading"><p className="eyebrow">Le sur mesure / votre point de départ</p><h1>Vous avez l’idée.<br /><em>Dessinons la suite.</em></h1><p>Un logo, une plaque différente, un cadeau en petite série. Un projet commence par un usage, pas par un fichier à téléverser.</p>{selected && <p className="notice">Votre point de départ : {selected.name}. Ce choix est indicatif, aucune demande n’a été envoyée.</p>}</div><ModelPreview product={sample} /></section>
    <div className="info-layout section"><section><p className="eyebrow">Avant la conversation</p><h2>Les bons repères.</h2><ol className="project-checklist"><li><span>01</span>Le type d’objet et l’endroit où il sera utilisé.</li><li><span>02</span>Le texte exact et les graphies à conserver.</li><li><span>03</span>Les dimensions, les couleurs et la quantité souhaitées.</li><li><span>04</span>Pour un logo : un fichier dont vous détenez les droits.</li><li><span>05</span>Votre date souhaitée, sans engagement de délai à ce stade.</li></ol></section><section className="info-panel"><span className="panel-number">Une étude, pas une promesse automatique</span><h2>Chaque détail compte.</h2><p>L’atelier devra vérifier la lisibilité, la solidité, la stabilité et la possibilité d’imprimer le projet. Le prix final dépendra de cette étude.</p><p className="notice">Les demandes de devis ouvriront plus tard. Aucun formulaire, fichier ou renseignement personnel n’est collecté ici.</p><Link className="text-link" href="/contact">Voir les coordonnées de l’atelier ↗</Link></section></div>
    <p className="muted">Envie d’un point de départ plus simple ?</p><Link className="button" href="/shop">Personnaliser un objet de la collection ↗</Link></div>;
}
```

## Fichier app/error.tsx

```tsx
'use client';

import Link from 'next/link';

export default function ErrorPage({ reset }: { reset: () => void }) {
  return <div className="shell section empty-state"><p className="eyebrow">Une interruption inattendue</p><h1>Reprenons le fil.</h1><p>La page n’a pas pu être affichée. Réessayez ou revenez à la collection.</p><button className="button" type="button" onClick={reset}>Réessayer ↗</button><p><Link className="text-link" href="/shop">Retrouver la boutique</Link></p></div>;
}
```

## Fichier app/globals.css

```css
@import "tailwindcss";

.commercial-media img { display: block; width: 100%; height: auto; aspect-ratio: 4 / 5; object-fit: cover; }
.qr-preview { display: grid; place-items: center; width: 100%; height: 100%; background: #fff; color: #161616; }
.qr-preview img { display: block; width: 100%; height: 100%; object-fit: contain; }
.qr-preview span { padding: .5rem; font-size: 10px; text-align: center; }
.card-action { display: inline-block; color: var(--blue); font-size: .75rem; margin-block-start: .8rem; }
.shop-layout { display: grid; grid-template-columns: 210px minmax(0, 1fr); gap: 2rem; align-items: start; }
.shop-sidebar { position: sticky; inset-block-start: 1rem; }
.shop-filters { display: grid; gap: .5rem; padding-block: .5rem; }
.shop-filters h2 { font-family: inherit; font-size: .9rem; margin-block: 0 .5rem; }
.filter-category { display: flex; justify-content: space-between; gap: .5rem; padding: .6rem; text-align: start; font-size: .8rem; border-radius: .3rem; }
.filter-category.selected { background: #eee5d6; color: #22232a; font-weight: 650; }
.filter-category span { font-size: .7rem; color: #6a6255; }
.filter-colors { display: grid; gap: .6rem; margin-block: 1.1rem; }
.filter-colors legend { margin-block-end: .8rem; font-size: .85rem; font-weight: 650; }
.filter-colors label { display: flex; align-items: center; gap: .5rem; font-size: .8rem; min-height: 28px; }
.filter-swatch { display: inline-block; width: 16px; height: 16px; border: 1px solid #aaa; border-radius: 50%; }
.filter-note { color: #6a6255; font-size: .75rem; line-height: 1.6; margin-block: 1rem; }
.shop-results { min-width: 0; }
.shop-results .results-heading { margin-block-start: 0; }
.shop-grid .card-title { flex-wrap: wrap; gap: .5rem; }
.shop-grid .card-title h3 { font-size: 1rem; }
.shop-grid .card-copy > p:not(.eyebrow) { font-size: .8rem; }
.shop-grid .card-visual .product-art svg { aspect-ratio: 4 / 5; object-fit: contain; }
.mobile-filter-row { display: none; }
.filter-dialog { position: fixed; inset: 0; margin: auto; width: min(90vw, 440px); max-height: 90dvh; overflow: auto; background: #faf7ef; color: #22232a; border: 1px solid #dbd1bf; padding: 1.3rem; }
.filter-dialog::backdrop { background: #22232a88; }
.filter-dialog header { display: flex; justify-content: space-between; align-items: center; }
.filter-dialog header button { font-size: 1.8rem; padding: .5rem; }
@media (min-width: 1440px) { .shop-layout .shop-grid { grid-template-columns: repeat(4, minmax(0, 1fr)); } }
@media (min-width: 761px) and (max-width: 1150px) { .shop-layout .shop-grid { grid-template-columns: repeat(2, minmax(0, 1fr)); } }
@media (max-width: 760px) {
  .shop-layout { grid-template-columns: minmax(0, 1fr); }
  .shop-sidebar { display: none; }
  .mobile-filter-row { display: flex; justify-content: space-between; align-items: center; gap: 1rem; margin-block: 1rem; font-size: .8rem; }
  .filter-trigger { border: 1px solid #aaa; padding: .7rem; border-radius: .3rem; }
  .filter-dialog .filter-colors label { min-height: 44px; }
}
@media (max-width: 359px) { .shop-layout .shop-grid { grid-template-columns: minmax(0, 1fr); } }

.model-preview img { display: block; width: 100%; height: auto; aspect-ratio: 4 / 3; object-fit: contain; }
.product-gallery > .model-preview { padding-block: 0; }

:root { --paper: #faf8f2; --ink: #292b2c; --blue: #3047a5; --sand: #eee7da; --line: #dcd8cd; --muted: #6d6c65; --soft-blue: #e9ecf7; }
* { box-sizing: border-box; }
html { scroll-behavior: smooth; scroll-padding-top: 2rem; }
body { margin: 0; background: var(--paper); color: var(--ink); font-family: "Trebuchet MS", Arial, "Segoe UI", sans-serif; line-height: 1.65; -webkit-font-smoothing: antialiased; }
h1, h2, h3, p, figure { margin: 0; }
h1, h2, h3 { font-weight: 500; line-height: 1.12; letter-spacing: -.045em; text-wrap: balance; }
h1 { font-size: clamp(2.8rem, 5vw, 5rem); }
h2 { font-size: clamp(2rem, 3.3vw, 3.3rem); }
h3 { font-size: 1.3rem; letter-spacing: -.025em; }
em { font-family: Georgia, "Times New Roman", serif; font-weight: 400; color: var(--blue); }
a { color: inherit; text-decoration: none; }
button, input, select, textarea { font: inherit; }
button { color: inherit; }
button:not(:disabled), summary { cursor: pointer; }
button:disabled { cursor: not-allowed; opacity: .5; }
button { border: 0; background: none; }
a, button, input, select, summary { -webkit-tap-highlight-color: transparent; }
a:hover { color: var(--blue); }
:focus-visible { outline: 2px solid var(--blue); outline-offset: 5px; }
::selection { color: white; background: var(--blue); }
main:focus { outline: none; }
.shell { width: min(100% - 5rem, 1280px); margin-inline: auto; }
.skip { position: fixed; inset-block-start: 1rem; inset-inline-start: 1rem; transform: translateY(-200%); background: white; padding: .75rem 1rem; z-index: 10; }
.skip:focus { transform: none; }
.contact-bar { background: var(--blue); color: #fff; font-size: .72rem; letter-spacing: .025em; }
.contact-bar .shell, .contact-bar .shell > div { display: flex; align-items: center; gap: 1.6rem; }
.contact-bar .shell { justify-content: space-between; min-height: 38px; }
.contact-bar a:hover { color: white; text-decoration: underline; }
.contact-bar :focus-visible { outline-color: white; }
.contact-bar a, .cart-trigger { display: inline-flex; align-items: center; min-height: 38px; }
.cart-trigger { gap: .4rem; color: white; padding-inline: 0; }
.site-header { border-block-end: 1px solid var(--line); }
.topbar { display: flex; align-items: center; justify-content: space-between; gap: 2rem; min-height: 94px; }
.wordmark { display: inline-flex; align-items: center; gap: .6rem; font-size: 1.25rem; font-weight: 700; letter-spacing: -.06em; white-space: nowrap; }
.wordmark svg { color: var(--blue); }
.brand-dot { width: 5px; height: 5px; background: var(--blue); border-radius: 50%; align-self: flex-end; margin-block-end: 10px; margin-inline-start: -4px; }
.navigation { display: flex; gap: 1.8rem; align-items: center; font-size: .85rem; }
.navigation a { padding-block: 1rem; }
.navigation [aria-current] { color: var(--blue); }
.nav-contact { border-inline-start: 1px solid var(--line); padding-inline-start: 2rem; }
.nav-contact span { margin-inline-start: 1rem; }
.menu-button { display: none; }
.hero { display: grid; grid-template-columns: .97fr 1.03fr; gap: 3rem; align-items: center; padding-block: 3.2rem 3.5rem; }
.hero h1 { margin-block: 1.5rem; font-size: clamp(3.1rem, 5.6vw, 5.4rem); line-height: 1.01; letter-spacing: -.06em; }
.hero-copy > p:not(.eyebrow):not(.hero-note) { font-size: .97rem; color: var(--muted); max-width: 39ch; line-height: 1.85; }
.eyebrow { font-size: .66rem; font-weight: 700; letter-spacing: .16em; text-transform: uppercase; color: var(--blue); line-height: 1.6; }
.tiny-line { display: inline-block; width: 1.8rem; height: 1px; background: currentColor; vertical-align: middle; margin-inline-end: .7rem; }
.hero-actions { display: flex; align-items: center; flex-wrap: wrap; gap: 1.7rem; margin-block: 1.8rem; }
.button { background: var(--blue); color: #fff; display: inline-flex; justify-content: space-between; align-items: center; gap: 1.6rem; padding: .95rem 1.35rem; border: 1px solid transparent; font-size: .85rem; font-weight: 600; min-height: 50px; transition: transform .2s ease, background .2s ease; }
.button:hover { background: #253b8e; color: #fff; }
.button:active { transform: translateY(1px); }
.text-link { font-size: .85rem; font-weight: 600; text-decoration: underline; text-decoration-thickness: 1px; text-underline-offset: .4em; }
.hero-note { font-size: .68rem; color: var(--muted); }
.hero-note span { padding-inline: .65rem; }
.hero-stage { min-width: 0; position: relative; background: #ece7dc; aspect-ratio: 1.05; isolation: isolate; }
.stage-top, .stage-bottom { position: absolute; inset-inline: 1.5rem; display: flex; justify-content: space-between; gap: .8rem; font-size: .51rem; letter-spacing: .12em; color: #777468; z-index: 1; }
.stage-top { inset-block-start: 1.2rem; }
.stage-bottom { inset-block-end: 1.2rem; letter-spacing: .04em; }
.hero-orbit { position: absolute; inset: 12% 11%; border: 1px solid #d4cbb9; border-radius: 50%; transform: rotate(-30deg); }
.hero-orbit::before, .hero-orbit::after { content: ""; position: absolute; border: 1px solid #d4cbb9; border-radius: 50%; inset: 6%; }
.hero-orbit::after { inset: 12%; }
.hero-key { position: absolute; width: 94%; inset-block-start: 1%; inset-inline-start: 8%; transform: rotate(4deg); }
.hero-desk { position: absolute; width: 66%; inset-block-end: 1%; inset-inline-start: -2%; transform: rotate(-4deg); }
.hero-label { position: absolute; inset-block-end: 22%; inset-inline-end: 5%; display: flex; align-items: center; gap: .7rem; font-size: .64rem; line-height: 1.5; color: #646358; }
.mini-cross { font-size: 1.8rem; font-weight: 300; color: var(--blue); }
.hero-stage .product-art { background: none; }
.hero-stage figcaption { display: none; }
.manifesto-strip { background: var(--sand); border-block: 1px solid #e2dacb; }
.manifesto-strip .shell { display: flex; align-items: center; justify-content: space-between; gap: 1rem; min-height: 63px; font-size: .69rem; color: #68685f; }
.manifesto-strip span:first-child { font-family: Georgia, serif; font-style: italic; font-size: 1.15rem; color: var(--ink); }
.section { margin-block: clamp(3.5rem, 6vw, 6rem); }
.section-heading { display: flex; align-items: flex-end; justify-content: space-between; gap: 1rem; margin-block-end: 2rem; }
.section-heading h2 { margin-block-start: .6rem; }
.section-heading > .text-link { margin-block-end: .4rem; white-space: nowrap; }
.grid-cards { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 2.3rem 1.5rem; }
.featured-grid { display: grid; grid-template-columns: 1.18fr 1fr 1fr; gap: 1.5rem; }
.card { min-width: 0; }
.card-link { display: block; }
.card-visual { position: relative; overflow: hidden; }
.product-art { background: #eee8dd; margin: 0; position: relative; min-width: 0; }
.product-art svg { display: block; width: 100%; height: auto; transition: transform .45s cubic-bezier(.16,1,.3,1); }
.product-art figcaption { text-align: center; font-size: .5rem; color: #716c61; padding-block-end: .8rem; letter-spacing: .04em; }
.art-label { display: flex; flex-direction: column; justify-content: center; align-items: center; height: 100%; width: 100%; font-family: "Trebuchet MS", "Segoe UI", Tahoma, Arial, sans-serif; font-weight: 700; line-height: 1.25; text-align: center; padding: 2px; overflow-wrap: anywhere; }
.art-label bdi { max-width: 100%; }
.art-plaque-bureau { background: #e8e9df; }
.art-support-qr { background: #e5e7ea; }
.art-ville-maroc { background: #ede1d3; }
.art-logo-bureau { background: #e3e6e4; }
.art-plaque-porte { background: #eee4dd; }
.card-arrow { display: grid; place-items: center; background: #fff8; border: 1px solid #fff7; width: 35px; height: 35px; border-radius: 50%; position: absolute; inset-inline-end: 1rem; inset-block-end: 1rem; transition: background .2s; }
.card a:hover svg { transform: scale(1.035); }
.card a:hover .card-arrow { background: var(--blue); color: white; }
.card-copy { padding-block: 1.1rem .5rem; }
.card-copy .eyebrow { font-size: .58rem; }
.card-title { display: flex; justify-content: space-between; gap: .75rem; margin-block: .45rem .4rem; align-items: baseline; }
.card-title h3 { font-size: 1.15rem; }
.card-title > span { white-space: nowrap; font-size: .8rem; }
.card-copy > p:not(.eyebrow) { font-size: .77rem; color: var(--muted); }
.card-copy small { color: var(--muted); font-size: .62rem; display: block; margin-block-start: .4rem; }
.collection-grid { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 1px; background: var(--line); border: 1px solid var(--line); }
.collection { background: var(--paper); display: grid; grid-template-columns: auto 1fr auto; gap: 1.5rem; padding: 2rem; align-items: center; transition: background .2s; }
.collection:hover { background: var(--sand); }
.collection-number { color: var(--muted); font-size: .65rem; font-family: monospace; align-self: start; padding-block-start: .3rem; }
.collection h3 { font-size: 1.45rem; }
.collection p { font-size: .76rem; color: var(--muted); margin-block-start: .35rem; }
.collection > span:last-child { font-size: 1.5rem; font-weight: 300; color: var(--blue); }
.atelier { display: grid; grid-template-columns: 1.05fr .95fr; align-items: center; gap: 5rem; }
.atelier-art { position: relative; background: #ede1d3; padding-block: 3rem; }
.atelier-stamp { position: absolute; inset-inline-start: 1.8rem; inset-block-start: 1.5rem; font-family: Georgia, serif; font-size: 1.3rem; font-style: italic; line-height: 1.2; color: #947456; }
.atelier-copy h2 { margin-block: .7rem 1.4rem; font-size: clamp(2.6rem, 4vw, 4rem); }
.atelier-copy p:not(.eyebrow) { color: var(--muted); font-size: .88rem; margin-block: 1rem; }
.atelier-copy .text-link { display: inline-block; margin-block-start: .8rem; }
.steps { list-style: none; padding: 0; display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 2.5rem; }
.steps li { border-block-start: 1px solid var(--line); padding-block-start: 1.1rem; }
.steps li > span { color: var(--blue); font-size: .7rem; display: block; margin-block-end: 1.7rem; }
.steps p { color: var(--muted); font-size: .85rem; margin-block-start: .8rem; max-width: 32ch; }
.business-banner { background: var(--blue); color: white; padding: 3rem 4rem; display: grid; grid-template-columns: 1.4fr 1fr; align-items: center; gap: 3rem; overflow: hidden; }
.business-banner .eyebrow { color: #d2d9fa; }
.business-banner h2 { margin-block: 1rem; }
.business-banner p:not(.eyebrow) { color: #dce1f5; font-size: .87rem; max-width: 48ch; }
.button-light { background: var(--paper); color: var(--blue); margin-block-start: 1.6rem; }
.button-light:hover { background: #e5e7f2; color: var(--blue); }
.business-art .product-art { background: transparent; }
.business-art figcaption { color: #dce1f5; }
.business-art { transform: rotate(7deg) scale(1.2); }
.faq { display: grid; grid-template-columns: .8fr 1.2fr; gap: 5rem; }
.faq h2 { margin-block-start: 1rem; }
details { border-block-start: 1px solid var(--line); padding-block: 1.1rem; font-size: .88rem; }
details:last-child { border-block-end: 1px solid var(--line); }
summary { list-style: none; display: flex; justify-content: space-between; align-items: center; gap: 1rem; min-height: 30px; font-weight: 600; }
summary::-webkit-details-marker { display: none; }
summary::after { content: "+"; font-size: 1.4rem; color: var(--blue); }
details[open] summary::after { content: "−"; }
details p { color: var(--muted); margin-block-start: .8rem; max-width: 65ch; }
.footer { border-block-start: 1px solid var(--line); background: #f0ede5; padding-block: 3rem 1.2rem; margin-block-start: 5rem; }
.footer-top { display: flex; justify-content: space-between; align-items: center; gap: 2rem; padding-block-end: 2.5rem; }
.footer-top p { font-size: .85rem; }
.footer-top p span { color: var(--muted); }
.footer-bottom { border-block-start: 1px solid var(--line); padding-block-start: 1.2rem; display: flex; flex-wrap: wrap; align-items: center; justify-content: space-between; gap: 1rem; font-size: .63rem; color: var(--muted); }
.footer-bottom nav { display: flex; gap: 1.3rem; }
.page-content { min-height: 55vh; }
.page-heading { max-width: 850px; margin-block-end: 3rem; }
.page-heading h1 { margin-block: .8rem 1.2rem; }
.page-heading p:not(.eyebrow) { color: var(--muted); max-width: 55ch; font-size: .95rem; }
.collection-tabs { display: flex; align-items: center; gap: .5rem; flex-wrap: wrap; border-block-end: 1px solid var(--line); padding-block-end: 1rem; }
.collection-tabs > * { font-size: .79rem; padding: .55rem 1rem; border: 1px solid transparent; min-height: 42px; }
.collection-tabs [aria-current], .collection-tabs [aria-pressed="true"] { background: var(--blue); color: white; }
.collection-tabs a span { opacity: .65; padding-inline-start: .7rem; font-size: .65rem; }
.catalogue-controls { display: grid; grid-template-columns: 1fr 240px; gap: 1.5rem; margin-block: 1.5rem; }
.field { display: grid; gap: .45rem; font-size: .8rem; font-weight: 600; min-width: 0; }
.field input, .field select, .line-actions input { border: 1px solid #b3afa3; border-radius: 0; background: #fff9; color: var(--ink); padding: .75rem .9rem; min-height: 48px; width: 100%; min-width: 0; }
.field input:focus, .field select:focus { background: white; }
input[dir="auto"] { font-family: "Segoe UI", Tahoma, Arial, sans-serif; font-size: 1rem; }
.field small { font-size: .68rem; font-weight: 400; }
.field-error { color: #94402c; }
.results-heading { display: flex; justify-content: space-between; gap: 1rem; align-items: center; font-size: .75rem; color: var(--muted); margin-block: 1.8rem; }
.catalogue-note { border-block-start: 1px solid var(--line); font-size: .72rem; color: var(--muted); padding-block-start: 1.2rem; margin-block-start: 3rem; }
.empty-state { padding: 3rem 1rem; text-align: center; }
.empty-state h1, .empty-state h2, .empty-state h3 { margin-block: 1rem; }
.empty-state p { max-width: 48ch; margin-inline: auto; font-size: .9rem; color: var(--muted); }
.empty-state .button { margin-block-start: 1.5rem; }
.empty-mark { display: inline-grid; place-items: center; width: 55px; height: 55px; border: 1px solid var(--line); border-radius: 50%; color: var(--blue); font-family: Georgia, serif; font-size: 2rem; }
.breadcrumbs { display: flex; flex-wrap: wrap; gap: .7rem; font-size: .73rem; color: var(--muted); margin-block-end: 2rem; }
.breadcrumbs a { color: var(--blue); }
.product-layout { display: grid; grid-template-columns: 1.05fr .95fr; gap: 4.5rem; align-items: start; }
.product-copy h1 { font-size: clamp(2.4rem, 3.5vw, 3.5rem); margin-block: .8rem 1rem; }
.product-copy > p:not(.eyebrow) { font-size: .86rem; color: var(--muted); }
.product-copy .product-tagline { font-size: 1rem; }
.product-price { font-size: 1.6rem; margin-block: 1.2rem; }
.product-price small { font-size: .65rem; color: var(--muted); margin-inline-start: .8rem; }
.product-gallery > .product-art { padding-block: 3rem; }
.gallery-caption { display: flex; justify-content: space-between; flex-wrap: wrap; gap: .3rem; font-size: .6rem; color: var(--muted); margin-block: .8rem 1.8rem; }
.product-gallery details { font-size: .8rem; }
.personalizer { display: grid; gap: 1rem; margin-block-start: 2rem; border-block-start: 1px solid var(--line); padding-block-start: 1.6rem; }
.config-heading { display: flex; justify-content: space-between; align-items: center; gap: 1rem; margin-block-end: .4rem; }
.config-heading h2 { font-size: 1.5rem; }
.config-heading > span { font-size: .6rem; color: var(--muted); font-family: monospace; }
fieldset { padding: 0; margin: 0; border: 0; min-width: 0; }
legend { font-size: .75rem; font-weight: 600; margin-block-end: .6rem; }
.options { display: flex; flex-wrap: wrap; gap: .4rem; }
.option { flex: 1; display: flex; justify-content: center; align-items: center; gap: .5rem; border: 1px solid var(--line); padding: .65rem .8rem; font-size: .77rem; cursor: pointer; min-height: 44px; }
.option input, .palette input { accent-color: var(--blue); }
.option.selected { border-color: var(--blue); background: var(--soft-blue); color: var(--blue); }
.palette-options { display: grid; gap: .5rem; margin-block-start: .5rem; }
.palette { display: flex; gap: .7rem; align-items: center; padding: .65rem .85rem; border: 1px solid var(--line); font-size: .74rem; cursor: pointer; }
.palette.selected { border-color: var(--blue); background: #f0f1f6; }
.palette small { display: block; font-size: .6rem; color: var(--muted); }
.swatches { display: flex; min-width: 62px; }
.swatches > span { width: 18px; height: 18px; border-radius: 50%; border: 1px solid #49433933; margin-inline-end: -4px; }
.live-preview { background: var(--sand); padding: 1rem; min-width: 0; }
.preview-heading { display: flex; align-items: center; justify-content: space-between; gap: 1rem; font-size: .6rem; color: var(--muted); }
.live-preview .product-art { background: none; }
.live-preview svg { max-height: 205px; }
.preview-spelling { font-size: .75rem; display: flex; flex-direction: column; gap: .25rem; align-items: center; text-align: center; overflow-wrap: anywhere; }
.preview-spelling bdi { max-width: 100%; }
.preview-spelling a { color: var(--blue); text-decoration: underline; margin-block-start: .5rem; }
.quantity-total { display: flex; align-items: end; justify-content: space-between; gap: 1rem; }
.quantity { max-width: 112px; }
.quantity-total output { text-align: end; line-height: 1.4; font-size: .8rem; }
.quantity-total output span { display: block; color: var(--muted); font-size: .68rem; }
.quantity-total output strong { font-size: 1.5rem; font-weight: 500; }
.full-width { width: 100%; }
.demo-note { font-size: .68rem; color: var(--muted); }
.notice { border-inline-start: 2px solid var(--blue); padding: .8rem 1rem; background: var(--soft-blue); font-size: .8rem; line-height: 1.65; }
.notice p + p { margin-block-start: .5rem; }
.related-grid { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 1.5rem; max-width: 870px; }
.bespoke-block { background: var(--sand); margin-block-start: 2rem; padding: 1.5rem; }
.bespoke-block h3 { margin-block: .7rem; }
.bespoke-block p { font-size: .8rem; }
.bespoke-block .button { margin-block-start: 1.2rem; }
.drawer { position: fixed; inset: 0 0 0 auto; inset-inline-start: auto; inset-inline-end: 0; margin: 0; width: min(100%, 490px); max-width: 100%; height: 100dvh; max-height: 100dvh; overflow: auto; padding: 1.6rem; background: var(--paper); color: var(--ink); border: 0; overscroll-behavior: contain; }
.drawer::backdrop { background: #292b2c66; backdrop-filter: blur(3px); }
.drawer header { display: flex; justify-content: space-between; align-items: center; gap: .6rem; border-block-end: 1px solid var(--line); padding-block-end: 1.2rem; margin-block-end: 1rem; }
.drawer h2 { font-size: 1.8rem; margin-block-start: .4rem; }
.close-button { font-size: 1.7rem; border: 1px solid var(--line); width: 42px; height: 42px; flex-shrink: 0; }
.cart-lines { padding: 0; list-style: none; margin: 0; }
.cart-line { padding-block: 1.4rem; border-block-end: 1px solid var(--line); display: grid; grid-template-columns: 95px minmax(0,1fr); gap: 1rem; }
.cart-thumbnail { align-self: start; }
.cart-line-copy { min-width: 0; }
.cart-line h3 { font-size: 1rem; margin-block-end: .3rem; }
.cart-options { display: flex; flex-direction: column; font-size: .82rem; overflow-wrap: anywhere; }
.cart-options bdi { max-width: 100%; }
.cart-line-copy > p { font-size: .66rem; margin-block: .25rem; }
.cart-line-copy > strong { font-size: .8rem; font-weight: 600; }
.line-actions { display: flex; flex-wrap: wrap; gap: .4rem 1rem; align-items: end; margin-block-start: .7rem; font-size: .7rem; }
.line-actions label { display: grid; gap: .2rem; font-size: .62rem; }
.line-actions input { width: 67px; padding: .3rem .5rem; min-height: 40px; }
.line-actions > a, .line-actions > button { text-decoration: underline; text-underline-offset: 3px; min-height: 40px; padding-block: .5rem; }
.cart-total { display: flex; align-items: baseline; justify-content: space-between; gap: .75rem; margin-block: 1.5rem 1rem; font-size: .85rem; }
.cart-total strong { font-size: 1.3rem; font-weight: 500; }
.drawer > .muted { font-size: .72rem; }
.drawer .full-width { margin-block: 1.2rem; }
.cart-suggestions { margin-block-start: 2rem; }
.cart-suggestions > a { display: flex; justify-content: space-between; gap: 1rem; align-items: center; padding-block: .8rem; border-block-end: 1px solid var(--line); font-size: .75rem; }
.cart-suggestions small { display: block; color: var(--muted); font-size: .62rem; }
.info-layout { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 2rem; margin-block: 2rem; }
.info-panel { background: var(--sand); padding: 2.5rem; min-width: 0; }
.info-panel.plain { background: none; border: 1px solid var(--line); }
.panel-number { color: var(--muted); font-size: .66rem; }
.info-panel h2 { font-size: 2rem; margin-block: 1.5rem; }
.info-panel p { font-size: .85rem; margin-block: 1rem; }
.info-panel .text-link { display: inline-block; margin-block: .8rem; }
.contact-links { display: grid; gap: 1rem; color: var(--blue); overflow-wrap: anywhere; }
.editorial-intro { display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: center; }
.editorial-intro .page-heading { margin: 0; }
.project-checklist { padding: 0; list-style: none; margin-block: 1.5rem; }
.project-checklist li { padding-block: 1rem; border-block-start: 1px solid var(--line); display: flex; gap: 1rem; align-items: baseline; font-size: .88rem; }
.project-checklist span { color: var(--blue); font-size: .65rem; min-width: 1rem; }
.business-examples { display: grid; grid-template-columns: 1.2fr 1fr; gap: 1.5rem; }
.checkout-layout { display: grid; grid-template-columns: 1.3fr .7fr; gap: 4rem; align-items: start; }
.checkout-layout .cart-line { grid-template-columns: 140px minmax(0, 1fr); }
.checkout-summary { background: var(--sand); padding: 2rem; }
.checkout-summary h2 { font-size: 1.5rem; }
.checkout-summary .button { margin-block-start: 1.5rem; }
.checkout-summary p { font-size: .8rem; margin-block-start: 1rem; }
.muted { color: var(--muted); }
.loading-block { padding: 2.5rem 1rem; background: var(--sand); color: var(--muted); font-size: .8rem; animation: breathe 1.5s ease-in-out infinite alternate; }
@keyframes breathe { to { opacity: .6; } }
@media (min-width: 1450px) { .hero { gap: 5rem; padding-block: 4rem; } }
@media (max-width: 1050px) {
  .shell { width: calc(100% - 3rem); }
  .navigation { gap: 1rem; font-size: .75rem; }
  .nav-contact { padding-inline-start: 1rem; }
  .hero { gap: 2rem; }
  .hero h1 { font-size: clamp(3rem, 6vw, 4.5rem); }
  .hero-stage { aspect-ratio: .9; }
  .hero-key { inset-block-start: 7%; }
  .hero-desk { width: 80%; inset-block-end: 8%; }
  .hero-label { inset-block-end: 17%; font-size: .55rem; }
  .featured-grid { grid-template-columns: repeat(3,minmax(0,1fr)); gap: 1rem; }
  .card-title { flex-wrap: wrap; gap: .2rem; }
  .atelier, .product-layout { gap: 2.5rem; }
  .business-banner { padding: 2.5rem; gap: 1rem; }
  .info-panel { padding: 1.5rem; }
  .checkout-layout { gap: 2rem; }
}
@media (max-width: 760px) {
  .shell { width: calc(100% - 2rem); }
  .contact-bar { font-size: .62rem; }
  .contact-bar .shell { flex-wrap: wrap; justify-content: space-between; gap: 0 .7rem; padding-block: .1rem; }
  .contact-bar .shell > div { gap: 1rem; }
  .configured-contact { display: none !important; }
  .contact-bar .shell > span { padding-block: .2rem; }
  .topbar { min-height: 76px; flex-wrap: wrap; gap: 0; }
  .wordmark { font-size: 1.15rem; }
  .menu-button { display: block; min-height: 44px; padding: .5rem 0 .5rem .7rem; font-size: .75rem; }
  .navigation { display: none; width: 100%; padding-block: .5rem 1rem; grid-template-columns: 1fr 1fr; border-block-start: 1px solid var(--line); gap: 0 1rem; }
  .navigation.is-open { display: grid; }
  .navigation a { padding-block: .7rem; min-height: 44px; }
  .nav-contact { border: 0; padding-inline: 0; }
  .hero { grid-template-columns: 1fr; gap: 2rem; padding-block: 2.5rem 2rem; }
  .hero h1 { font-size: clamp(3.25rem, 10vw, 4.6rem); margin-block: 1rem; }
  .hero-copy > p:not(.eyebrow):not(.hero-note) { font-size: .9rem; max-width: 45ch; }
  .hero-actions { margin-block: 1.5rem 1rem; gap: 1rem 1.5rem; }
  .hero-stage { aspect-ratio: 1.18; max-width: 550px; width: 100%; justify-self: center; }
  .hero-key { inset-block-start: -7%; width: 87%; inset-inline-start: 15%; }
  .hero-desk { width: 67%; inset-block-end: -2%; }
  .hero-label { inset-block-end: 22%; font-size: .58rem; }
  .stage-top, .stage-bottom { inset-inline: 1rem; font-size: .45rem; }
  .manifesto-strip .shell { flex-wrap: wrap; justify-content: flex-start; gap: .4rem 1rem; padding-block: 1rem; font-size: .61rem; }
  .manifesto-strip span:first-child { flex-basis: 100%; margin-block-end: .3rem; }
  .section { margin-block: 3.4rem; }
  .section-heading { align-items: start; flex-wrap: wrap; gap: 1rem; margin-block-end: 1.5rem; }
  h2 { font-size: 2.1rem; }
  .featured-grid, .grid-cards { grid-template-columns: repeat(2,minmax(0,1fr)); gap: 1.8rem 1rem; }
  .featured-grid > :first-child { grid-column: 1/-1; }
  .featured-grid > :first-child .product-art svg { max-height: 300px; }
  .card-copy { padding-block-start: .8rem; }
  .card-title h3 { font-size: 1.05rem; }
  .card-copy > p:not(.eyebrow) { font-size: .7rem; line-height: 1.6; }
  .card-arrow { width: 28px; height: 28px; inset-block-end: .6rem; inset-inline-end: .6rem; font-size: .8rem; }
  .collection-grid, .atelier, .business-banner, .faq, .product-layout, .info-layout, .editorial-intro, .checkout-layout { grid-template-columns: 1fr; }
  .collection { padding: 1.4rem 1rem; gap: 1rem; }
  .collection h3 { font-size: 1.35rem; }
  .atelier { gap: 2rem; }
  .atelier-art { padding-block: 2rem 0; }
  .atelier-copy h2 { font-size: 2.8rem; }
  .steps { grid-template-columns: 1fr; gap: 1.5rem; }
  .steps li { display: grid; grid-template-columns: 30px 1fr; gap: 0 .75rem; }
  .steps li > span { grid-row: 1/3; margin: 0; }
  .steps p { max-width: none; grid-column: 2; margin-block-start: .5rem; }
  .business-banner { padding: 2rem 1.5rem; gap: .5rem; }
  .business-art { max-width: 300px; width: 100%; justify-self: center; transform: rotate(6deg); }
  .faq { gap: 1.5rem; }
  .footer { margin-block-start: 3rem; padding-block-start: 2rem; }
  .footer-top { flex-wrap: wrap; align-items: start; gap: 1.3rem 2rem; }
  .footer-top > .text-link { flex-basis: 100%; }
  .footer-bottom { display: grid; gap: .8rem; }
  .page-heading h1 { font-size: clamp(2.5rem, 8vw, 3.8rem); }
  .page-heading { margin-block-end: 2rem; }
  .catalogue-controls { grid-template-columns: 1fr 145px; gap: .75rem; }
  .catalogue-controls .field { font-size: .7rem; }
  .catalogue-controls input, .catalogue-controls select { padding-inline: .65rem; font-size: .8rem; }
  .collection-tabs { gap: .3rem; }
  .collection-tabs > * { padding: .5rem .7rem; font-size: .72rem; }
  .results-heading { font-size: .65rem; }
  .results-heading .text-link { font-size: .65rem; }
  .product-layout { gap: 2rem; }
  .product-gallery > .product-art { padding-block: 0; }
  .product-copy h1 { font-size: 2.6rem; }
  .product-price small { display: block; margin-inline-start: 0; }
  .related-grid { gap: 1rem; }
  .info-layout { gap: 1rem; }
  .info-panel { padding: 1.5rem; }
  .business-examples { grid-template-columns: 1fr 1fr; gap: 1rem; }
  .checkout-layout .cart-line { grid-template-columns: 90px minmax(0,1fr); gap: .7rem; }
}
@media (max-width: 360px) {
  .contact-bar .shell { display: grid; grid-template-columns: 1fr auto; gap: .4rem; }
  .contact-bar .shell > span { max-width: 155px; font-size: .58rem; line-height: 1.4; }
  .contact-bar .shell > div { gap: .65rem; }
  .wordmark { font-size: 1.05rem; gap: .4rem; }
  .wordmark svg { width: 24px; }
  .hero h1 { font-size: 3.1rem; }
  .hero-actions .text-link { font-size: .77rem; }
  .hero-note { font-size: .58rem; }
  .hero-note span { padding-inline: .3rem; }
  .hero-stage { aspect-ratio: 1; }
  .hero-key { inset-block-start: 1%; width: 96%; inset-inline-start: 5%; }
  .hero-desk { width: 79%; inset-block-end: 3%; }
  .hero-label { inset-block-end: 26%; font-size: .5rem; }
  .stage-bottom { font-size: .39rem; }
  .grid-cards { grid-template-columns: 1fr; }
  .featured-grid { gap: 1.5rem .75rem; }
  .featured-grid .card-copy > p:not(.eyebrow) { display: none; }
  .card-copy .eyebrow { font-size: .5rem; letter-spacing: .1em; }
  .card-title { display: grid; }
  .featured-grid .card-title h3 { font-size: .95rem; }
  .catalogue-controls { grid-template-columns: 1fr; }
  .option { padding-inline: .45rem; font-size: .71rem; }
  .drawer { padding: 1rem; }
  .drawer h2 { font-size: 1.5rem; }
  .cart-line { grid-template-columns: 67px minmax(0,1fr); gap: .7rem; }
  .line-actions { gap: .3rem .6rem; }
  .palette { padding-inline: .6rem; gap: .5rem; font-size: .7rem; }
  .related-grid, .business-examples { grid-template-columns: 1fr; }
}
@media (prefers-reduced-motion: reduce) { html { scroll-behavior: auto; } *, *::before, *::after { animation: none !important; transition: none !important; } }
```

## Fichier app/layout.tsx

```tsx
import type { Metadata } from 'next';
import Link from 'next/link';
import './globals.css';
import { Cart } from './cart';
import { getProducts } from '../lib/catalogue.server';
import { getOperatingMode } from '../lib/mode.server';
import { brand, contactLinks } from '../lib/brand';
import { Navigation } from './navigation';

export const metadata: Metadata = {
  title: { default: 'MustDesign3D | Des objets qui parlent de vous', template: '%s | MustDesign3D' },
  description: 'Objets personnalisés, prénoms arabes et français, cadeaux et accessoires de bureau. Découvrez la collection de démonstration MustDesign3D, au Maroc.',
};

export default function Layout({ children }: Readonly<{ children: React.ReactNode }>) {
  return <html lang="fr"><body><Cart products={getProducts()} isDemo={getOperatingMode().isDemo} contacts={contactLinks()}>
    <Navigation />
    <main id="contenu" tabIndex={-1}>{children}</main>
    <footer className="footer"><div className="shell">
      <div className="footer-top"><Link href="/" className="wordmark">{brand.name}<span className="brand-dot" /></Link><p>Des objets qui parlent de vous.<br /><span>Imaginés pour le Maroc.</span></p><Link className="text-link" href="/custom">Une idée en tête ? Parlons design ↗</Link></div>
      <div className="footer-bottom"><span>© 2026 MustDesign3D · Collection de démonstration</span><nav aria-label="Pied de page"><Link href="/shop">Boutique</Link><Link href="/business">Professionnels</Link><Link href="/contact">Contact</Link></nav><span>Pas de commande ni de paiement en ligne.</span></div>
    </div></footer>
  </Cart></body></html>;
}
```

## Fichier app/loading.tsx

```tsx
export default function Loading() {
  return <div className="shell section"><div className="loading-block" role="status">Votre prochaine idée prend forme…</div></div>;
}
```

## Fichier app/model-preview.tsx

```tsx
'use client';

import Image from 'next/image';
import { useState } from 'react';
import type { Product } from '../lib/contracts';
import { ProductArt } from './product-art';

export function ModelPreview({ product }: { product: Product }) {
  const [failed, setFailed] = useState(false);
  const image = product.images[0];
  if (!image || failed) return <ProductArt product={product} />;
  return <figure className="model-preview product-art">
    <Image src={image.src} alt={image.alt} width={720} height={540} sizes="(max-width: 760px) 95vw, 45vw" onError={() => setFailed(true)} />
    <figcaption>Vue du fichier OpenSCAD · prototype à valider</figcaption>
  </figure>;
}
```

## Fichier app/modeles/page.tsx

```tsx
import Link from 'next/link';
import { getModelProducts } from '../../lib/catalogue.server';
import { ModelPreview } from '../model-preview';

export const metadata = { title: 'Nos modèles 3D', description: 'Les prototypes originaux MustDesign3D, du fichier paramétrique à la composition de votre objet.' };

export default function ModelsPage() {
  return <div className="shell section page-content">
    <p className="eyebrow">Dans les coulisses de l’atelier</p>
    <h1>Du dessin au volume.</h1>
    <p>Découvrez les vues des sept prototypes originaux MustDesign3D. Chaque image est générée à partir de son fichier paramétrique OpenSCAD.</p>
    <p className="notice">La géométrie a été exportée en STL pour contrôle. Les temps d’impression, la résistance et les assemblages restent à valider dans Bambu Studio puis sur l’A1.</p>
    <section className="section grid-cards" aria-label="Modèles de la collection">
      {getModelProducts().map(product => <article className="card" key={product.id}><Link href={'/product/' + product.slug}><ModelPreview product={product} /><div className="card-copy"><h2>{product.name}</h2><p>Fichier de prototype · contrôle de fabrication à poursuivre</p></div></Link></article>)}
    </section>
    <section className="feature section"><h2>Une base pour votre idée.</h2><p>Un prénom, une ville, une plaque professionnelle ou un motif pixel. L’atelier adapte les dimensions et la composition après vérification du prototype.</p><Link className="button" href="/custom">Préparer mon projet ↗</Link></section>
  </div>;
}
```

## Fichier app/navigation.tsx

```tsx
'use client';

import Link from 'next/link';
import { usePathname } from 'next/navigation';
import { useState } from 'react';
import { brand, labels } from '../lib/brand';

export function Navigation() {
  const [open, setOpen] = useState(false);
  const pathname = usePathname();
  const links = [{ href: '/shop', label: labels.shop }, { href: '/modeles', label: 'Modèles 3D' }, { href: '/business', label: labels.business }, { href: '/custom', label: labels.custom }];
  return <header className="site-header"><div className="shell topbar">
    <Link href="/" className="wordmark" onClick={() => setOpen(false)} aria-label={brand.name + ' · accueil'}><svg viewBox="0 0 32 32" width="28" height="28" aria-hidden="true"><path d="M3 23V9l7 4 6-9 6 9 7-4v14l-13 6Z" fill="none" stroke="currentColor" strokeWidth="1.7" /><path d="m3 23 13-8 13 8M16 15v14" fill="none" stroke="currentColor" strokeWidth="1.7" /></svg>{brand.name}<span className="brand-dot" /></Link>
    <button type="button" className="menu-button" aria-expanded={open} aria-controls="main-nav" onClick={() => setOpen(!open)} onKeyDown={event => { if (event.key === 'Escape') setOpen(false); }}>{open ? 'Fermer ×' : 'Menu +'}</button>
    <nav id="main-nav" className={open ? 'navigation is-open' : 'navigation'} aria-label="Navigation principale" onKeyDown={event => { if (event.key === 'Escape') { setOpen(false); document.querySelector<HTMLButtonElement>('.menu-button')?.focus(); } }}>{links.map(link => <Link key={link.href} href={link.href} aria-current={pathname === link.href ? 'page' : undefined} onClick={() => setOpen(false)}>{link.label}</Link>)}<Link className="nav-contact" href="/contact" onClick={() => setOpen(false)}>Une idée ? <span aria-hidden="true">↗</span></Link></nav>
  </div></header>;
}
```

## Fichier app/not-found.tsx

```tsx
import Link from 'next/link';

export default function NotFound() {
  return <div className="shell section empty-state"><p className="eyebrow">404 / Une forme introuvable</p><h1>Cet objet reste<br /><em>à imaginer.</em></h1><p>Cette page n’existe pas. Retrouvez les créations de démonstration dans la collection.</p><Link className="button" href="/shop">Retrouver la collection ↗</Link></div>;
}
```

## Fichier app/page.tsx

```tsx
import Link from 'next/link';
import { getProducts } from '../lib/catalogue.server';
import { collections } from '../lib/products';
import { ProductArt, ProductCard } from './product-card';

export default function Home() {
  const products = getProducts();
  return <>
    <div className="shell">
      <section className="hero">
        <div className="hero-copy"><p className="eyebrow"><span className="tiny-line" /> Le détail qui change tout</p>
          <h1>Un peu de vous.<br />Beaucoup de<br /><em>caractère.</em></h1>
          <p>Un prénom, une ville, une idée. Nous leur donnons du relief avec des objets personnalisés, pensés pour votre quotidien.</p>
          <div className="hero-actions"><Link className="button" href="/product/porte-cles-prenom">Créer mon aperçu <span aria-hidden="true">↗</span></Link><Link className="text-link" href="/shop">Explorer la collection →</Link></div>
          <p className="hero-note">Français & arabe <span>·</span> Vos couleurs <span>·</span> Votre signature</p>
        </div>
        <div className="hero-stage">
          <div className="stage-top"><span>OBJETS SINGULIERS / VOL. 01</span><span>MD—3D</span></div>
          <div className="hero-orbit" aria-hidden="true" />
          <div className="hero-key"><ProductArt product={products[0]} /></div>
          <div className="hero-desk"><ProductArt product={products[1]} /></div>
          <div className="hero-label"><span className="mini-cross" aria-hidden="true">+</span><span>Votre prénom.<br />Dans votre écriture.</span></div>
          <div className="stage-bottom"><span>DESIGN PERSONNALISÉ</span><span>Illustrations originales · démo 2D</span></div>
        </div>
      </section>
    </div>
    <div className="manifesto-strip"><div className="shell"><span>Petites séries, grandes idées.</span><span>01 / Choisir</span><span>02 / Personnaliser</span><span>03 / Imaginer chez soi</span></div></div>
    <div className="shell">
      <section className="section"><div className="section-heading"><div><p className="eyebrow">Les premières signatures</p><h2>À chacun son objet.</h2></div><Link className="text-link" href="/shop">Toute la collection <span aria-hidden="true">↗</span></Link></div>
        <div className="featured-grid">{products.filter(product => product.featured).map(product => <ProductCard key={product.id} product={product} />)}</div>
      </section>
      <section id="collections" className="section"><div className="section-heading"><div><p className="eyebrow">Trois façons de se retrouver</p><h2>Un objet. Votre univers.</h2></div><Link className="text-link" href="/modeles">Explorer les modèles 3D ↗</Link></div>
        <div className="collection-grid">{collections.map((collection, index) => <Link className={'collection collection-' + index} key={collection.id} href={'/shop?category=' + collection.id}><span className="collection-number">0{index + 1}</span><div><h3>{collection.label}</h3><p>{collection.note}</p></div><span aria-hidden="true">↗</span></Link>)}</div>
      </section>
      <section className="section atelier"><div className="atelier-art"><ProductArt product={products[2]} /><span className="atelier-stamp">Le Maroc,<br />en filigrane.</span></div><div className="atelier-copy"><p className="eyebrow">L’esprit MustDesign3D</p><h2>Du sens.<br />De la matière.<br /><em>Du relief.</em></h2><p>Nous explorons une idée simple : les objets les plus attachants racontent quelque chose de nous. Une graphie familière, une couleur choisie, une ville qu’on garde près de soi.</p><p>Cette première collection est une invitation à composer. Les illustrations sont originales ; les prototypes restent à valider à l’atelier avant de devenir des objets à commander.</p><Link className="text-link" href="/custom">Découvrir le sur mesure ↗</Link></div></section>
      <section className="section"><div className="section-heading"><div><p className="eyebrow">C’est vous qui donnez le ton</p><h2>Trois gestes. Votre signature.</h2></div></div><ol className="steps">
        <li><span>01</span><h3>Trouvez votre forme.</h3><p>Une attention à offrir, une plaque à poser ou un détail pour votre commerce.</p></li>
        <li><span>02</span><h3>Ajoutez votre histoire.</h3><p>Votre prénom, vos mots. En français, en arabe, ou les deux pour le porte-clés.</p></li>
        <li><span>03</span><h3>Essayez les couleurs.</h3><p>Composez dans l’aperçu et gardez vos idées dans votre panier démo.</p></li>
      </ol></section>
      <section id="professionnels" className="section business-banner"><div><p className="eyebrow">Pour les lieux qui ont une identité</p><h2>Votre marque mérite<br />aussi du relief.</h2><p>Plaques, supports QR et petites séries : imaginez les détails qui donnent le ton à votre espace.</p><Link className="button button-light" href="/business">Explorer les projets professionnels ↗</Link></div><div className="business-art"><ProductArt product={products[3]} /></div></section>
      <section id="faq" className="section faq"><div><p className="eyebrow">Tout simplement</p><h2>Avant de<br />vous lancer.</h2></div><div>
        <details><summary>Mon prénom peut-il être écrit en arabe ?</summary><p>Oui. Le porte-clés propose le français, l’arabe et un mode bilingue avec deux graphies distinctes. L’aperçu conserve votre écriture ; le tracé final sera vérifié avant fabrication.</p></details>
        <details><summary>Est-ce que je peux passer commande ?</summary><p>Pas encore. Cette collection est une démo locale : explorez, personnalisez et conservez votre composition sans fournir de coordonnées ni effectuer de paiement.</p></details>
        <details><summary>Les visuels montrent-ils des objets déjà fabriqués ?</summary><p>Ce sont des illustrations 2D originales de concepts. Les dimensions, la tenue, les couleurs et la qualité d’impression devront être confirmées sur prototype.</p></details>
        <details><summary>Et pour un logo ou une petite série ?</summary><p>Le parcours sur mesure explique les informations à préparer. Aucun fichier ni renseignement personnel n’est collecté dans cette démo.</p><Link href="/custom">Préparer un projet →</Link></details>
      </div></section>
    </div>
  </>;
}
```

## Fichier app/product-art.tsx

```tsx
import { useId, type CSSProperties } from 'react';
import type { Personalization, Product } from '../lib/contracts';
import { graphemeCount } from '../lib/validation';
import { labels } from '../lib/brand';
import { QrPreview } from './qr-preview';

export function ProductArt({ product, personalization, compact = false }: { product: Product; personalization?: Personalization; compact?: boolean }) {
  const unique = useId().replace(/:/g, '');
  const palette = product.palettes.find(option => personalization && 'paletteId' in personalization && option.id === personalization.paletteId) ?? product.palettes[0];
  const [base, ink, trim = ink] = palette.colors;
  const names = personalization?.kind === 'name' ? [personalization.frenchName, personalization.arabicName].filter((name): name is string => name !== null) : product.slug === 'porte-cles-prenom' ? ['Meryem', 'مريم'] : [personalization?.kind === 'text' ? personalization.text : product.mark];
  const size = Math.max(11, Math.min(39, 340 / Math.max(7, ...names.map(name => graphemeCount(name))) * 1.6));
  const renderLabel = (position: { x: number; y: number; width: number; height: number }, small = false) => <foreignObject {...position}><div className="art-label" style={{ color: ink, fontSize: small ? Math.min(size, 24) : size }}>{names.map((name, index) => <bdi dir="auto" key={index}>{name || (product.personalizationSchema.kind === 'name' ? 'Votre prénom' : 'Votre texte')}</bdi>)}</div></foreignObject>;
  return <figure className={'product-art art-' + product.slug + (compact ? ' art-compact' : '')} style={{ '--piece-base': base } as CSSProperties}>
    <svg viewBox="0 0 500 360" role="img" aria-label={product.name + ' · illustration originale de démonstration'}>
      <defs>
        <linearGradient id={'surface-' + unique} x1="0" y1="0" x2="1" y2="1"><stop stopColor="#ffffff" stopOpacity=".65" /><stop offset="1" stopColor="#cabda7" stopOpacity=".35" /></linearGradient>
        <linearGradient id={'metal-' + unique} x1="0" x2="1" y1="0" y2="1"><stop stopColor="#e5e4df" /><stop offset=".4" stopColor="#8a8a85" /><stop offset=".7" stopColor="#f4f3e9" /><stop offset="1" stopColor="#777b7c" /></linearGradient>
        <filter id={'shadow-' + unique} x="-50%" y="-50%" width="200%" height="220%"><feDropShadow dx="2" dy="16" stdDeviation="11" floodColor="#524333" floodOpacity=".22" /></filter>
        <pattern id={'layers-' + unique} width="4" height="3" patternUnits="userSpaceOnUse"><path d="M0 2.5H4" stroke="#fff" strokeOpacity=".17" strokeWidth=".5" /></pattern>
      </defs>
      <ellipse cx="260" cy="291" rx="160" ry="20" fill="#6e614d" opacity=".07" />
      {product.slug === 'plaque-pixel-zellige' && <g filter={'url(#shadow-' + unique + ')'}>
        <rect x="132" y="64" width="236" height="236" rx="12" fill={base} />
        <path d="m250 86 38 70 70 26-70 28-38 70-38-70-70-28 70-26Z" fill={ink} />
        <rect x="226" y="158" width="48" height="48" fill={trim} />
      </g>}
      {product.slug === 'porte-cles-prenom' && <g transform="rotate(-12 250 180)" filter={'url(#shadow-' + unique + ')'}>
        <circle cx="110" cy="126" r="42" fill="none" stroke={'url(#metal-' + unique + ')'} strokeWidth="9" /><circle cx="110" cy="126" r="35" fill="none" stroke="#fff" strokeOpacity=".6" strokeWidth="1" />
        <rect x="115" y="153" width="310" height="117" rx="36" fill={ink} /><rect x="115" y="144" width="310" height="117" rx="36" fill={trim} /><rect x="119" y="140" width="302" height="113" rx="32" fill={base} />
        <rect x="126" y="147" width="288" height="99" rx="27" fill={'url(#layers-' + unique + ')'} /><circle cx="138" cy="170" r="8" fill="#b2a591" /><circle cx="138" cy="168" r="6" fill="#eee8dc" />
        <path d="m132 162-15-17" stroke={'url(#metal-' + unique + ')'} strokeWidth="6" />{renderLabel({ x: 157, y: 150, width: 239, height: 88 })}
      </g>}
      {product.slug === 'plaque-bureau' && <g filter={'url(#shadow-' + unique + ')'}>
        <path d="m83 265 33-43h302l-28 43Z" fill={trim} /><path d="M83 265h307v15H83Z" fill={ink} /><path d="m390 265 28-43v15l-28 43Z" fill="#a27d43" />
        <path d="m114 227 7-112h278l-7 112Z" fill={ink} /><rect x="103" y="108" width="284" height="128" rx="9" fill={base} /><rect x="112" y="117" width="266" height="110" rx="5" fill={'url(#layers-' + unique + ')'} />
        {renderLabel({ x: 119, y: 126, width: 250, height: 64 })}<text x="244" y="209" textAnchor="middle" fill={ink} fontSize="11" letterSpacing="3">VOTRE ESPACE, VOTRE SIGNATURE</text><path d="M215 220h60" stroke={trim} strokeWidth="2" />
      </g>}
      {product.slug === 'ville-maroc' && <g filter={'url(#shadow-' + unique + ')'}>
        <path d="M74 254v-91h39v-42h48V96h35v84h22v-42h28V64h27v22h19v103h19v-45h50v-28h34v138Z" fill={trim} />
        <path d="M80 254v-87h40v-42h48v-25h35v84h22v-42h28V68h27v22h19v103h19v-45h50v-28h34v134Z" fill={base} />
        <path d="M135 252v-51c0-33 48-33 48 0v51m133 0v-32c0-25 35-25 35 0v32" fill={ink} /><path d="M129 252v-52c0-41 60-41 60 0v52" fill="none" stroke={trim} strokeWidth="6" />
        <path d="M263 111h9m-9 17h9m-9 17h9M206 254v-32h17v32" stroke={ink} strokeWidth="4" /><path d="M71 255h339v20H71Z" fill={ink} /><rect x="71" y="249" width="339" height="18" rx="3" fill={trim} />
        {renderLabel({ x: 88, y: 280, width: 310, height: 43 }, true)}
      </g>}
      {product.slug === 'support-qr' && <g filter={'url(#shadow-' + unique + ')'}>
        <path d="m146 284 39-37h176l-27 37Z" fill={trim} /><path d="M146 284h188v12H146Z" fill={ink} /><path d="m334 284 27-37v12l-27 37Z" fill="#b78a49" />
        <path d="M179 255V92q0-20 20-20h119q20 0 20 20v163Z" fill={ink} /><path d="M166 249V84q0-20 20-20h119q20 0 20 20v165Z" fill={base} />
        <rect x="188" y="102" width="115" height="115" fill="#fff" />
        <foreignObject x="188" y="102" width="115" height="115"><QrPreview url={personalization?.kind === 'qr' ? personalization.url : 'https://example.com/menu'} /></foreignObject>
        <foreignObject x="188" y="78" width="115" height="22"><div className="art-label" style={{ color: ink, fontSize: 10 }}><bdi dir="auto">{personalization?.kind === 'qr' ? personalization.businessName : 'Votre commerce'}</bdi></div></foreignObject>
        <text x="245" y="236" textAnchor="middle" fill={ink} fontSize="9">{personalization?.kind === 'qr' ? { menu: 'MENU', website: 'SITE WEB', social: 'RÉSEAUX', reviews: 'AVIS', other: 'INFORMATION' }[personalization.destinationType] : 'SCANNER LE QR'}</text>
      </g>}
      {product.slug === 'logo-bureau' && <g filter={'url(#shadow-' + unique + ')'}>
        <path d="m105 267 31-32h254l-24 32Z" fill={trim} /><path d="M105 267h261v15H105Z" fill={ink} /><path d="M139 237V115l46 20 54-69 51 69 61-20v122Z" fill={ink} />
        <path d="M129 227V105l46 20 54-69 51 69 61-20v122Z" fill={base} /><path d="m155 204 74-107 74 107m-127-34h106" fill="none" stroke={ink} strokeWidth="14" strokeLinejoin="round" /><path d="M229 98v125" stroke={trim} strokeWidth="5" />
        <text x="235" y="306" textAnchor="middle" fill={ink} fontSize="12" letterSpacing="3">MONOGRAMME ORIGINAL MD</text>
      </g>}
      {product.slug === 'plaque-porte' && <g transform="rotate(-5 250 180)" filter={'url(#shadow-' + unique + ')'}>
        <rect x="81" y="122" width="348" height="144" rx="61" fill={ink} /><rect x="74" y="112" width="348" height="144" rx="61" fill={trim} /><rect x="80" y="114" width="336" height="132" rx="56" fill={base} /><rect x="92" y="126" width="312" height="108" rx="47" fill="none" stroke={trim} strokeWidth="2" />
        <circle cx="106" cy="180" r="4" fill={ink} /><circle cx="391" cy="180" r="4" fill={ink} />{renderLabel({ x: 123, y: 143, width: 252, height: 74 })}
        <path d="m240 132 8-8 8 8-8 8Z" fill={trim} />
      </g>}
      {product.slug === 'porte-cles-plaque-marocaine' && <g transform="rotate(-7 250 180)" filter={'url(#shadow-' + unique + ')'}>
        <circle cx="91" cy="154" r="26" fill="none" stroke={'url(#metal-' + unique + ')'} strokeWidth="6" />
        <rect x="100" y="139" width="320" height="95" rx="12" fill={ink} />
        <rect x="105" y="140" width="310" height="85" rx="10" fill={base} />
        <rect x="116" y="151" width="288" height="63" rx="4" fill="none" stroke={ink} strokeWidth="2" />
        {renderLabel({ x: 127, y: 153, width: 266, height: 60 }, true)}
      </g>}
      {product.slug === 'etiquette-sac' && <g transform="rotate(-12 250 180)" filter={'url(#shadow-' + unique + ')'}>
        <path d="M140 113h245v138H140l-50-69Z" fill={ink} />
        <path d="M140 106h245v138H140l-50-69Z" fill={base} />
        <circle cx="126" cy="175" r="8" fill={ink} />
        <path d="M126 175C45 155 38 96 89 91" fill="none" stroke="#6c6256" strokeWidth="6" />
        {renderLabel({ x: 158, y: 137, width: 201, height: 75 })}
      </g>}
      {product.slug === 'plaque-contact' && <g filter={'url(#shadow-' + unique + ')'}>
        <rect x="92" y="101" width="325" height="164" rx="15" fill={ink} />
        <rect x="86" y="93" width="325" height="164" rx="15" fill={base} />
        {renderLabel({ x: 107, y: 136, width: 283, height: 77 }, true)}
        <path d="M178 236h139" stroke={ink} strokeWidth="3" />
      </g>}
      {product.slug === 'marque-places-personnalises' && <g filter={'url(#shadow-' + unique + ')'}>
        {['Nour', 'Lina', 'Amine'].map((name, index) => <g key={name} transform={'translate(' + (80 + index * 104) + ' ' + (110 + index * 24) + ')'}>
          <path d="M0 0h140l-15 94H-15Z" fill={base} stroke={ink} strokeWidth="2" />
          <text x="60" y="55" fill={ink} textAnchor="middle" fontSize="25">{name}</text>
        </g>)}
      </g>}
      {product.slug === 'porte-cles-logo-lot' && <g filter={'url(#shadow-' + unique + ')'}>
        {[0, 1, 2].map(index => <g key={index} transform={'translate(' + (87 + index * 108) + ' ' + (110 + index * 25) + ') rotate(-12)'}>
          <circle cx="15" cy="-3" r="20" fill="none" stroke={'url(#metal-' + unique + ')'} strokeWidth="5" />
          <rect x="0" y="12" width="116" height="90" rx="15" fill={base} stroke={ink} strokeWidth="3" />
          <text x="58" y="72" fill={ink} textAnchor="middle" fontSize="38">MD</text>
        </g>)}
      </g>}
      <path d="M33 310h18m-9-9v18M450 45h18m-9-9v18" stroke="#988b77" strokeWidth="1" opacity=".45" />
    </svg>
    {!compact && <figcaption>{labels.preview}</figcaption>}
  </figure>;
}
```

## Fichier app/product-card.tsx

```tsx
import Link from 'next/link';
import { categoryLabel, productPrice, type Product } from '../lib/products';
import { ProductMedia } from './product-media';

export { ProductArt } from './product-art';

export function ProductCard({ product }: { product: Product }) {
  return <article className="card">
    <Link href={'/product/' + product.slug} className="card-link" aria-label={product.name + ' · ' + productPrice(product)}>
      <div className="card-visual"><ProductMedia product={product} /><span className="card-arrow" aria-hidden="true">↗</span></div>
      <div className="card-copy">
        <p className="eyebrow">{categoryLabel(product.categoryId)}</p>
        <div className="card-title"><h3>{product.name}</h3><span>{productPrice(product)}</span></div>
        <p>{product.shortDescription}</p><small>{product.pricingMode === 'quote' ? 'Série personnalisée · étude du projet' : 'Prix indicatif · collection démo'}</small>
        <span className="card-action">{product.pricingMode === 'quote' ? 'Préparer mon projet' : 'Personnaliser'} ↗</span>
      </div>
    </Link>
  </article>;
}
```

## Fichier app/product-media.tsx

```tsx
'use client';

import Image from 'next/image';
import { useState } from 'react';
import type { Product } from '../lib/contracts';
import { ProductArt } from './product-art';

export function ProductMedia({ product }: { product: Product }) {
  const [failed, setFailed] = useState(false);
  const image = product.images.find(item => item.kind === 'photo' || item.kind === 'generated-concept');
  if (!image || failed) return <ProductArt product={product} />;
  return <figure className="product-art commercial-media">
    <Image src={image.src} alt={image.alt} width={800} height={1000} sizes="(max-width: 760px) 50vw, 25vw" onError={() => setFailed(true)} />
    {image.kind === 'generated-concept' && <figcaption>Visualisation du concept</figcaption>}
  </figure>;
}
```

## Fichier app/product/[slug]/page.tsx

```tsx
import Link from 'next/link';
import { Suspense } from 'react';
import { notFound } from 'next/navigation';
import { getAllProducts, getProducts, getProductBySlug } from '../../../lib/catalogue.server';
import { categoryLabel, productPrice } from '../../../lib/products';
import { ProductCard } from '../../product-card';
import { Personalizer } from './personalizer';
import { ModelPreview } from '../../model-preview';
import { ProductMedia } from '../../product-media';

type Props = { params: Promise<{ slug: string }> };

export async function generateMetadata({ params }: Props) {
  const product = getProductBySlug((await params).slug);
  return { title: product?.name ?? 'Objet introuvable', description: product?.shortDescription };
}

export function generateStaticParams() {
  return getAllProducts().map(product => ({ slug: product.slug }));
}

export default async function ProductPage({ params }: Props) {
  const product = getProductBySlug((await params).slug);
  if (!product) notFound();
  const dimensions = product.dimensionsMm;
  return <div className="shell section page-content">
    <nav className="breadcrumbs" aria-label="Fil d’Ariane"><Link href="/shop">Collection</Link><span>/</span><span>{product.name}</span></nav>
    <div className="product-layout">
      <div className="product-gallery">{product.visibility === 'prototype' ? <ModelPreview product={product} /> : <ProductMedia product={product} />}<div className="gallery-caption"><span>{product.visibility === 'prototype' ? 'Vue du prototype par défaut' : 'Composition du concept'}</span><Link href="/modeles">Voir les prototypes ↗</Link></div><details><summary>Dimensions & matière</summary><p>{product.material}</p><p>{product.slug === 'porte-cles-prenom' ? 'Largeur indicative de la base : 65–85 mm · épaisseur : 3–4 mm.' : dimensions ? `${dimensions.width} × ${dimensions.depth} × ${dimensions.height} mm · dimensions du concept, indicatives.` : 'Dimensions à confirmer après étude du projet.'}</p><p>Couleurs, lisibilité, fixation et résistance à valider sur prototype. Les vues techniques et la personnalisation sont présentées séparément.</p></details></div>
      <div className="product-copy"><p className="eyebrow">{product.visibility === 'prototype' ? 'Étude de prototype' : categoryLabel(product.categoryId)} / Démonstration</p><h1>{product.name}</h1><p className="product-tagline">{product.shortDescription}</p><div className="product-price">{productPrice(product)} <small>{product.pricingMode === 'quote' ? 'Étude du projet à prévoir' : 'Prix indicatif'}</small></div><p>{product.description}</p>
        <Suspense fallback={<div className="loading-block" role="status">Préparation de votre composition…</div>}><Personalizer product={product} /></Suspense>
      </div>
    </div>
    <section className="section"><div className="section-heading"><div><p className="eyebrow">Dans le même esprit</p><h2>Les belles associations.</h2></div><Link className="text-link" href="/shop">Explorer la collection ↗</Link></div><div className="related-grid">{getProducts().filter(item => item.id !== product.id).sort((first, second) => Number(second.categoryId === product.categoryId) - Number(first.categoryId === product.categoryId)).slice(0, 2).map(item => <ProductCard key={item.id} product={item} />)}</div></section>
  </div>;
}
```

## Fichier app/product/[slug]/personalizer.tsx

```tsx
'use client';

import Link from 'next/link';
import { useSearchParams } from 'next/navigation';
import { useState, type FormEvent } from 'react';
import { useCart } from '../../cart';
import { ProductArt } from '../../product-art';
import type { CartLine, Personalization, Product, QrDestinationType } from '../../../lib/contracts';
import { formatPrice } from '../../../lib/products';
import { graphemeCount, isHttpsUrl, isQuantity, textError, validatePersonalization } from '../../../lib/validation';

export function Personalizer({ product }: { product: Product }) {
  const params = useSearchParams();
  const editId = params.get('edit');
  const cart = useCart();
  if (product.visibility === 'prototype' || product.pricingMode === 'quote' || product.personalizationSchema.kind === 'none') return <div className="bespoke-block"><p className="eyebrow">Une création à étudier ensemble</p><h3>Votre projet commence ici.</h3><p>Préparez les textes, les dimensions et la quantité souhaités. Pour un logo, choisissez un visuel dont vous détenez les droits. L’atelier vérifiera la faisabilité et le prix.</p><Link className="button" href={'/custom?product=' + product.slug}>Préparer mon projet ↗</Link></div>;
  if (!cart.ready) return <div className="loading-block" role="status">Préparation de votre composition…</div>;
  const editing = editId ? cart.lines.find(line => line.id === editId && line.productId === product.id) : undefined;
  if (editId && !editing) return <div className="notice" role="status"><p>Cette composition n’est plus dans le panier. Aucun autre article n’a été modifié.</p><Link href={'/product/' + product.slug}>Créer une nouvelle composition →</Link></div>;
  return <Configurator key={editId ?? product.id} product={product} initial={editing} />;
}

function Configurator({ product, initial }: { product: Product; initial?: CartLine }) {
  const cart = useCart();
  const previous = initial?.personalization;
  const [language, setLanguage] = useState<'fr' | 'ar' | 'both'>(previous?.kind === 'name' ? previous.language : 'fr');
  const [french, setFrench] = useState(previous?.kind === 'name' ? previous.frenchName ?? '' : '');
  const [arabic, setArabic] = useState(previous?.kind === 'name' ? previous.arabicName ?? '' : '');
  const [text, setText] = useState(previous?.kind === 'text' ? previous.text : '');
  const [url, setUrl] = useState(previous?.kind === 'qr' ? previous.url : '');
  const [businessName, setBusinessName] = useState(previous?.kind === 'qr' ? previous.businessName : '');
  const [destinationType, setDestinationType] = useState<QrDestinationType>(previous?.kind === 'qr' ? previous.destinationType : 'menu');
  const [paletteId, setPaletteId] = useState(previous && 'paletteId' in previous ? previous.paletteId : product.palettes[0].id);
  const [quantity, setQuantity] = useState(String(initial?.quantity ?? 1));
  const [submitError, setSubmitError] = useState('');
  const schema = product.personalizationSchema;
  const options: Personalization = schema.kind === 'name' ? { version: 1, kind: 'name', language, frenchName: language === 'ar' ? null : french, arabicName: language === 'fr' ? null : arabic, paletteId }
    : schema.kind === 'text' ? { version: 1, kind: 'text', text, paletteId } : { version: 1, kind: 'qr', businessName, destinationType, url, paletteId };
  const valid = validatePersonalization(product, options);
  const units = Number(quantity);
  const validQuantity = quantity.trim() !== '' && isQuantity(units);
  const maximum = schema.kind === 'name' || schema.kind === 'text' ? schema.maxGraphemes : 24;
  function submit(event: FormEvent) {
    event.preventDefault();
    if (!valid || !validQuantity) return;
    setSubmitError(cart.save(product.id, valid, units, initial?.id) ?? '');
  }
  return <form className="personalizer" onSubmit={submit} noValidate>
    <div className="config-heading"><h2>{initial ? 'Modifier ma composition' : 'À vous de composer.'}</h2><span>01 — 03</span></div>
    {initial && <p className="notice">Vos modifications remplacent cette ligne du panier. Les autres compositions sont conservées.</p>}
    {schema.kind === 'name' && <><fieldset><legend>01 / La langue de votre prénom</legend><div className="options">{([{ id: 'fr', label: 'Français' }, { id: 'ar', label: 'Arabe' }, { id: 'both', label: 'Bilingue' }] as const).map(mode => <label key={mode.id} className={language === mode.id ? 'option selected' : 'option'}><input type="radio" name="language" checked={language === mode.id} onChange={() => setLanguage(mode.id)} />{mode.label}</label>)}</div></fieldset>
      {language !== 'ar' && <div className="field"><label htmlFor="french-name">Prénom en français</label><input id="french-name" dir="auto" autoComplete="off" value={french} placeholder="Meryem" aria-invalid={!!textError(french, maximum)} aria-describedby="french-help" onChange={event => setFrench(event.target.value)} /><small id="french-help" className={textError(french, maximum) ? 'field-error' : 'muted'}>{textError(french, maximum) ?? graphemeCount(french) + ' / ' + maximum + ' caractères visibles'}</small></div>}
      {language !== 'fr' && <div className="field"><label htmlFor="arabic-name">Prénom en arabe</label><input id="arabic-name" dir="auto" lang="ar" autoComplete="off" value={arabic} placeholder="مريم" aria-invalid={!!textError(arabic, maximum)} aria-describedby="arabic-help" onChange={event => setArabic(event.target.value)} /><small id="arabic-help" className={textError(arabic, maximum) ? 'field-error' : 'muted'}>{textError(arabic, maximum) ?? graphemeCount(arabic) + ' / ' + maximum + ' caractères visibles'}</small></div>}
    </>}
    {schema.kind === 'text' && <label className="field">01 / {schema.label}<input dir="auto" autoComplete="off" value={text} placeholder={schema.placeholder} aria-invalid={!!textError(text, maximum)} aria-describedby="text-help" onChange={event => setText(event.target.value)} /><small id="text-help" className={textError(text, maximum) ? 'field-error' : 'muted'}>{textError(text, maximum) ?? graphemeCount(text) + ' / ' + maximum + ' caractères visibles'}</small></label>}
    {schema.kind === 'qr' && <>
      <label className="field">01 / Nom de l’établissement<input dir="auto" autoComplete="organization" value={businessName} placeholder="L’atelier de Lina" aria-invalid={!!textError(businessName, 32)} aria-describedby="business-name-help" onChange={event => setBusinessName(event.target.value)} /><small id="business-name-help" className={textError(businessName, 32) ? 'field-error' : 'muted'}>{textError(businessName, 32) ?? graphemeCount(businessName) + ' / 32 caractères visibles'}</small></label>
      <label className="field">02 / Type de destination<select value={destinationType} onChange={event => setDestinationType(event.target.value as QrDestinationType)}><option value="menu">Menu ou carte</option><option value="website">Site web</option><option value="social">Réseau social</option><option value="reviews">Avis clients</option><option value="other">Autre page</option></select></label>
      <label className="field">03 / Votre lien HTTPS<input type="url" dir="ltr" autoComplete="url" value={url} placeholder="https://votre-site.ma/menu" aria-invalid={!isHttpsUrl(url)} aria-describedby="url-help" onChange={event => setUrl(event.target.value)} /><small className={!isHttpsUrl(url) ? 'field-error' : 'muted'} id="url-help">{isHttpsUrl(url) ? 'Lien conservé, sans visite automatique.' : 'Saisissez une URL HTTPS valide, sans identifiants, de 2 048 caractères maximum.'}</small></label>
    </>}
    <fieldset className="palette-options"><legend>02 / Votre palette</legend>{product.palettes.map(palette => <label key={palette.id} className={paletteId === palette.id ? 'palette selected' : 'palette'}><input type="radio" name="palette" checked={paletteId === palette.id} onChange={() => setPaletteId(palette.id)} /><span className="swatches" aria-hidden="true">{palette.colors.map(color => <span key={color} style={{ background: color }} />)}</span><span>{palette.label}<small>{palette.colors.length} couleurs</small></span></label>)}</fieldset>
    <section className="live-preview" aria-label="Aperçu de votre personnalisation"><div className="preview-heading"><span className="eyebrow">Votre composition</span><span>Aperçu 2D</span></div><ProductArt product={product} personalization={options} compact /><div className="preview-spelling" aria-live="polite">{schema.kind !== 'qr' ? (options.kind === 'name' ? [options.frenchName, options.arabicName] : options.kind === 'text' ? [options.text] : []).filter(Boolean).map((name, index) => <bdi dir="auto" key={index}>{name}</bdi>) : <><p>Le QR représente votre lien. Sa lecture sur l’objet imprimé sera vérifiée sur prototype.</p>{isHttpsUrl(url) && <a href={url} target="_blank" rel="noopener noreferrer">Ouvrir mon lien pour le vérifier ↗</a>}</>}</div></section>
    <div className="quantity-total"><label className="field quantity">03 / Quantité<input type="number" min={1} max={99} step={1} value={quantity} aria-invalid={!validQuantity} aria-describedby="quantity-help" onChange={event => setQuantity(event.target.value)} /></label><output aria-live="polite">{validQuantity && product.priceCents !== null ? <><span>Total indicatif</span><strong>{formatPrice(product.priceCents * units)}</strong></> : 'Quantité invalide'}</output></div>
    <small id="quantity-help" className={validQuantity ? 'muted' : 'field-error'}>De 1 à 99 exemplaires par composition.</small>
    {submitError && <p className="notice" role="alert">{submitError}</p>}
    <button className="button full-width" disabled={!valid || !validQuantity} type="submit">{initial ? 'Enregistrer les modifications' : 'Ajouter au panier démo'} <span aria-hidden="true">↗</span></button>
    {initial && <Link className="text-link" href={'/product/' + product.slug}>Annuler la modification</Link>}
    <p className="demo-note">Commandes bientôt disponibles. Votre composition reste sur cet appareil si le stockage local est disponible. Ce n’est pas une commande.</p>
  </form>;
}
```

## Fichier app/qr-preview.tsx

```tsx
'use client';

import Image from 'next/image';
import { useEffect, useState } from 'react';
import QRCode from 'qrcode';
import { isHttpsUrl } from '../lib/validation';

export function QrPreview({ url }: { url: string }) {
  const [result, setResult] = useState({ url: '', image: '' });
  const [failed, setFailed] = useState(false);
  useEffect(() => {
    let active = true;
    setFailed(false);
    if (isHttpsUrl(url)) {
      QRCode.toDataURL(url, { errorCorrectionLevel: 'M', margin: 4, width: 256, color: { dark: '#000000', light: '#ffffff' } })
        .then(image => { if (active) setResult({ url, image }); })
        .catch(() => { if (active) setFailed(true); });
    }
    return () => { active = false; };
  }, [url]);
  return <div className="qr-preview" role="group" aria-label="Aperçu QR">
    {isHttpsUrl(url) && result.url === url && result.image
      ? <Image unoptimized src={result.image} width={256} height={256} alt="QR du lien choisi" data-qr-value={url} />
      : <span role="status">{failed ? 'QR indisponible. Réessayez.' : isHttpsUrl(url) ? 'Création du QR…' : 'Saisissez un lien HTTPS'}</span>}
  </div>;
}
```

## Fichier app/shop/catalogue.tsx

```tsx
'use client';

import Link from 'next/link';
import { useRef, useState } from 'react';
import { useSearchParams } from 'next/navigation';
import { collections, categoryLabel, filamentColors, normalizeSearch, type Product } from '../../lib/products';
import { ProductCard } from '../product-card';

type FilterProps = {
  products: Product[];
  category: string;
  color: string;
  budget: string;
  update: (key: string, value: string) => void;
};

function Filters({ products, category, color, budget, update }: FilterProps) {
  return <div className="shop-filters">
    <h2>Collections</h2>
    <button type="button" className={!category ? 'filter-category selected' : 'filter-category'} onClick={() => update('category', '')}>Tous les objets <span>{products.length}</span></button>
    {collections.map(collection => <button className={category === collection.id ? 'filter-category selected' : 'filter-category'} type="button" key={collection.id} aria-pressed={category === collection.id} onClick={() => update('category', collection.id)}>
      {collection.label}<span>{products.filter(product => product.categoryId === collection.id).length}</span>
    </button>)}
    <fieldset className="filter-colors"><legend>Couleur disponible</legend>
      <label><input type="radio" name="catalogue-color" checked={!color} onChange={() => update('color', '')} /> Toutes</label>
      {filamentColors.map(option => <label key={option.id}>
        <input type="radio" name="catalogue-color" checked={color === option.id} onChange={() => update('color', option.id)} />
        <span className="filter-swatch" style={{ background: option.hex }} aria-hidden="true" />{option.label}
      </label>)}
    </fieldset>
    <label className="field">Budget<select aria-label="Budget" value={budget} onChange={event => update('budget', event.target.value)}>
      <option value="">Tous les prix</option>
      <option value="under-50">Moins de 50 MAD</option>
      <option value="50-100">De 50 à 100 MAD</option>
      <option value="100-plus">Plus de 100 MAD</option>
      <option value="quote">Sur devis</option>
    </select></label>
    <p className="filter-note">Palette de départ<br />Noir, blanc, bleu et rouge</p>
    <Link className="text-link" href="/modeles">Les prototypes de l’atelier ↗</Link>
  </div>;
}

export function Catalogue({ products }: { products: Product[] }) {
  const params = useSearchParams();
  const query = params.get('q') ?? '';
  const category = params.get('category') ?? '';
  const color = params.get('color') ?? '';
  const rawBudget = params.get('budget') ?? '';
  const budget = ['', 'under-50', '50-100', '100-plus', 'quote'].includes(rawBudget) ? rawBudget : '';
  const sort = params.get('sort') ?? 'featured';
  const dialog = useRef<HTMLDialogElement>(null);
  const [filtersOpen, setFiltersOpen] = useState(false);

  function update(key: string, value: string) {
    const next = new URLSearchParams(params.toString());
    if (value && !(key === 'sort' && value === 'featured')) next.set(key, value);
    else next.delete(key);
    const url = '/shop' + (next.size ? '?' + next.toString() : '');
    if (key === 'q') window.history.replaceState(null, '', url);
    else window.history.pushState(null, '', url);
  }

  const selectedColor = filamentColors.find(option => option.id === color);
  const matches = products.filter(product => {
    if (category && product.categoryId !== category) return false;
    if (color && (!selectedColor || !product.palettes.some(palette => palette.colors.includes(selectedColor.hex)))) return false;
    if (budget === 'quote' && product.pricingMode !== 'quote') return false;
    if (budget && budget !== 'quote') {
      if (product.priceCents === null) return false;
      if (budget === 'under-50' && product.priceCents >= 5000) return false;
      if (budget === '50-100' && (product.priceCents < 5000 || product.priceCents > 10000)) return false;
      if (budget === '100-plus' && product.priceCents <= 10000) return false;
    }
    return normalizeSearch(product.name + ' ' + product.description + ' ' + categoryLabel(product.categoryId)).includes(normalizeSearch(query.trim()));
  }).sort((first, second) => {
    if (first.priceCents === null || second.priceCents === null) return Number(first.priceCents === null) - Number(second.priceCents === null);
    if (sort === 'price-asc') return first.priceCents - second.priceCents;
    if (sort === 'price-desc') return second.priceCents - first.priceCents;
    return Number(second.featured) - Number(first.featured);
  });
  const active = !!(query || category || color || budget || sort !== 'featured');
  const filters = { products, category, color, budget, update };

  function openFilters() {
    dialog.current?.showModal();
    setFiltersOpen(true);
  }

  return <>
    <div className="catalogue-controls">
      <label className="field">Rechercher un objet<input type="search" placeholder="Un prénom, une plaque, une idée…" value={query} onChange={event => update('q', event.target.value)} /></label>
      <label className="field">Trier par<select value={['featured', 'price-asc', 'price-desc'].includes(sort) ? sort : 'featured'} onChange={event => update('sort', event.target.value)}>
        <option value="featured">Notre sélection</option><option value="price-asc">Prix croissant</option><option value="price-desc">Prix décroissant</option>
      </select></label>
    </div>
    <div className="mobile-filter-row"><button type="button" className="filter-trigger" aria-expanded={filtersOpen} aria-controls="mobile-filters" onClick={openFilters}>Filtrer la collection +</button><span>{matches.length} résultat(s)</span></div>
    <div className="shop-layout">
      <aside className="shop-sidebar" aria-label="Filtres du catalogue"><Filters {...filters} /></aside>
      <div className="shop-results">
        <div className="results-heading"><p role="status">{matches.length} objet{matches.length !== 1 ? 's' : ''}{category ? ' · ' + categoryLabel(category) : ''}</p>{active && <Link className="text-link" href="/shop">Réinitialiser les filtres ×</Link>}</div>
        {matches.length ? <div className="grid-cards shop-grid">{matches.map(product => <ProductCard key={product.id} product={product} />)}</div> : <div className="empty-state">
          <h2>Une autre idée à explorer.</h2><p>Aucun objet ne correspond à ces filtres.</p><Link className="button" href="/shop">Revoir la collection ↗</Link>
        </div>}
        <p className="catalogue-note">Collection de démonstration · prix indicatifs · visuels de concepts</p>
      </div>
    </div>
    <dialog id="mobile-filters" ref={dialog} className="filter-dialog" aria-labelledby="filters-title" onClose={() => setFiltersOpen(false)}>
      <header><h2 id="filters-title">Vos filtres</h2><button type="button" onClick={() => dialog.current?.close()} aria-label="Fermer les filtres">×</button></header>
      {filtersOpen && <Filters {...filters} />}
      <button className="button full-width" type="button" onClick={() => dialog.current?.close()}>Voir les {matches.length} résultat(s)</button>
    </dialog>
  </>;
}
```

## Fichier app/shop/page.tsx

```tsx
import { Suspense } from 'react';
import { getProducts } from '../../lib/catalogue.server';
import { Catalogue } from './catalogue';

export const metadata = { title: 'La collection' };

export default function Shop() {
  return <div className="shell section page-content">
    <div className="page-heading"><p className="eyebrow">La collection / 01</p><h1>Des objets.<br /><em>Pas n’importe lesquels.</em></h1><p>Six créations, quatre univers. Et autant de façons d’y mettre un peu de vous.</p></div>
    <Suspense fallback={<div className="loading-block" role="status">Préparation de la collection…</div>}><Catalogue products={getProducts()} /></Suspense>
  </div>;
}
```

## Fichier codex.md

````markdown
codex
Yes. For your project, I would **not** build the business around random complicated STL models. I would design the whole research process around one rule:

> **Every product recommended must first pass a Bambu A1 + AMS Lite manufacturability test, then a Morocco business test.**

Your A1 has a **256 × 256 × 256 mm build volume**, uses a **0.4 mm nozzle by default**, and with AMS Lite it can print with **up to four filaments/colors**. PLA and PETG are among the materials Bambu lists as ideal for the machine. [cdn1.bambulab.com](https://cdn1.bambulab.com/documentation/quick-start-f507128172bdf/Quick%20start%20guide%20-%20A1%20combo-EN.pdf?utm_source=chatgpt.com)

For actual preparation, **Bambu Studio should be your final validation step** because it supports multi-material/color assignment, multiple plates, auto-arrange, supports and detailed slicing. [GitHub](https://github.com/bambulab/BambuStudio?utm_source=chatgpt.com)

### The simplest tool stack

For you, I would use **Tinkercad → Bambu Studio → Bambu A1** for original simple products. Tinkercad is a free browser-based 3D-design tool and is much easier to learn than professional CAD. [Tinkercad](https://www.tinkercad.com/?utm_source=chatgpt.com)

Use **MakerWorld** mainly for inspiration, testing and finding existing printable concepts. But there is a very important business rule: a free model is **not automatically legal to sell**. MakerWorld now supports commercial-license memberships, and you must check the individual model's license before selling printed copies. [Bambu Lab Blog](https://blog.bambulab.com/empowering-our-creators-with-new-commercial-license-membership/?utm_source=chatgpt.com)

For your long-term business, the strongest strategy is actually to **create your own variations/models** rather than depending entirely on downloaded models.

## What looks strongest for Morocco

There is already real Moroccan evidence for personalized 3D-printed products. One Moroccan seller currently lists personalized name keychains, Moroccan license-plate keychains, name decorations, organizers, planters, lamps and business products; another sells Moroccan monuments, custom figurines, lightboxes, logo clocks and map products. [To7fa](https://to7fa.ma/en?utm_source=chatgpt.com)

That means I would initially investigate these three large families:

| Priority | Niche | Examples | A1 difficulty |
|---|---|---|---|
| 🥇 | **Personalized Moroccan Gifts** | Arabic/French name keychains, magnets, name plates, gifts | Very easy |
| 🥈 | **Home & Desk Personalization** | door signs, desk names, organizers, wall décor | Easy |
| 🥉 | **Business Branding** | QR stands, logo signs, desk signs, counter displays | Easy–Medium |

The sweet spot for you is **2.5D printing rather than complex figurines**: flat base + raised text/logo/design + 2–4 colors. It looks premium but remains extremely easy to manufacture.

For example:

**Black base → white Arabic text → green Moroccan element → red accent**

That uses the AMS Lite very effectively without creating a difficult sculpture.

I would initially avoid making your main business around highly detailed figurines, huge statues, support-heavy dragons, complex articulated models, lithophanes requiring special tuning, large lamps, or products containing many separate mechanical components.

---

## Your final master prompt

I would use the following as the permanent master prompt for this business.

# MASTER PROMPT
## MOROCCO 3D PRINTING PRODUCT & NICHE RESEARCH
### Bambu Lab A1 + AMS Lite — Maximum 4 Colors

Act as my:

- 3D-printing product researcher
- Moroccan ecommerce researcher
- Bambu Lab manufacturing expert
- product designer
- CAD/DFM specialist
- small manufacturing business strategist
- product profitability analyst
- competitor researcher
- trend researcher

Your objective is to help me build a profitable small 3D-printing business in Morocco using my existing printer.

Do NOT simply give me attractive 3D models.

Every proposed product must pass TWO tests:

1. MARKET TEST
2. MANUFACTURABILITY TEST

If a product has strong demand but is difficult or unreliable to manufacture on my machine, reject it.

If a product is extremely easy to print but has weak commercial potential, reject it.

I want the overlap:

HIGH DEMAND
+
HIGH PERCEIVED VALUE
+
EASY PRODUCTION
+
LOW PRINT FAILURE
+
GOOD PROFIT

---

# 1. MY MACHINE

My printer is:

Bambu Lab A1

with:

AMS Lite

Therefore I can use up to:

4 filament colors in the normal AMS Lite workflow.

Assume:

Build volume:
256 × 256 × 256 mm

Default nozzle:
0.4 mm

Primary materials:
PLA / PLA+

Secondary:
PETG when required

Bambu Studio will be used for final slicing and validation.

The products must be designed specifically around this machine.

---

# 2. MOST IMPORTANT RULE

DO NOT recommend models simply because they look impressive.

The product must be practical to manufacture repeatedly.

I want products that I can print:

10 times

50 times

100 times

without constantly fixing problems.

Production reliability is more important than artistic complexity.

---

# 3. SAFE PRODUCT ENVELOPE

Prefer products that stay approximately within:

220 × 220 × 220 mm

even though the printer can technically print larger.

Prefer smaller products whenever possible.

Ideal products should normally use:

20–150 g filament.

Products above this are allowed only when the selling price and margin clearly justify them.

---

# 4. MAXIMUM 4 COLORS

Every model must use:

1, 2, 3 or maximum 4 colors.

NEVER recommend a design that requires more than four simultaneous filament colors.

Prefer:

2–3 colors.

Use four colors only when the additional color significantly increases perceived value.

---

# 5. MULTICOLOR EFFICIENCY

AMS multicolor printing can increase:

- print time
- filament changes
- purge waste

Therefore prefer designs where colors are grouped intelligently.

BEST:

Different colors by large areas or by layers.

GOOD:

Raised text or graphics in another color.

ACCEPTABLE:

Several distinct colored regions.

BAD:

Hundreds of tiny alternating color regions on every layer.

Reject models where multicolor waste becomes economically unreasonable.

Estimate:

- color swaps
- purge waste
- extra print time

when possible.

---

# 6. DESIGN-FOR-MANUFACTURING RULES

Strongly favor:

- flat-bottom models
- stable bed contact
- minimal overhangs
- no supports
- simple geometry
- large readable details
- easy slicing
- easy personalization
- easy scaling
- easy color changes
- easy batch production

Prefer products that print directly on the build plate.

Avoid supports whenever reasonably possible.

If support is necessary, explain why.

---

# 7. DEFAULT PRINT STRATEGY

Assume as the baseline:

0.4 mm nozzle

0.20 mm layer height

PLA

standard Bambu A1 profile

AMS Lite when needed

Do not require:

0.2 mm nozzle

exotic filament

advanced manual calibration

painting

resin printing

sanding

complex finishing

unless the business opportunity clearly justifies it.

---

# 8. COMPLEXITY RATING

Give every proposed product a:

PRINT DIFFICULTY SCORE /10

Where:

1–2 = extremely easy

3–4 = easy

5–6 = moderate

7–8 = difficult

9–10 = very difficult

For Phase 1 of the business:

Prefer only:

1–4 /10.

Products scoring above 5 should normally be rejected.

---

# 9. PRINT FAILURE RISK

Evaluate:

- bed adhesion
- warping
- bridging
- overhangs
- thin parts
- tall narrow structures
- small text
- delicate details
- unsupported areas
- multipart alignment
- AMS color complexity

Score:

FAILURE RISK

Low / Medium / High.

Prefer:

LOW.

---

# 10. PRODUCT TYPES TO SEARCH

Do broad research.

Consider:

Personalized gifts

Arabic name products

French/Arabic products

Moroccan-themed products

Home décor

Desk accessories

Business accessories

Organization products

Keychains

Magnets

Signs

Door signs

Desk nameplates

QR-code stands

Logo displays

Wall decorations

Geometric art

Moroccan maps

City-themed products

Wedding products

Birthday products

Event products

Ramadan/Eid decorations

Corporate gifts

Teacher gifts

Student products

Office accessories

Gaming accessories

Phone accessories

Simple household solutions

Cable organization

Planters

Small vases

Small storage products

Custom promotional products

Custom business signage

But do not limit research to these categories.

Search for better opportunities.

---

# 11. MOROCCO FIRST

The target market is:

MOROCCO.

Research Moroccan demand first.

Study:

- Moroccan ecommerce stores
- Google results
- Google Trends Morocco
- Instagram/TikTok trends where searchable
- Facebook marketplace signals where accessible
- Jumia Morocco
- Avito where relevant
- local gift stores
- personalized gift businesses
- 3D-print businesses
- Moroccan Instagram businesses
- Moroccan décor stores
- wedding/event businesses
- corporate gift companies

Then compare with:

France

Spain

USA

Etsy

Amazon

international 3D-printing trends

to discover products that are successful abroad but still relatively uncommon in Morocco.

---

# 12. FIND IMPORTABLE TRENDS

This is important.

Search for products that:

are already proven in Europe/USA

BUT

are not yet heavily saturated in Morocco.

Look especially for trends that can be localized using:

Arabic

Darija

French

Moroccan names

Moroccan cities

Moroccan culture

Moroccan architecture

geometric patterns

personalization

local professions

local celebrations.

---

# 13. PERSONALIZATION ADVANTAGE

Prioritize products that can be customized.

Examples:

customer name

family name

business name

logo

Arabic text

French text

date

city

coordinates

short message

initials

colors.

Personalization reduces direct price comparison.

Score:

PERSONALIZATION POTENTIAL /10.

---

# 14. PERCEIVED VALUE

A product should not be evaluated based solely on filament cost.

Calculate:

PERCEIVED VALUE / MATERIAL COST.

Look for products where:

10–30 MAD of material

can potentially become:

80 MAD

120 MAD

150 MAD

200 MAD+

of perceived customer value.

Do not invent prices.

Research Moroccan competitors first.

---

# 15. PRODUCT ECONOMICS

For every serious candidate estimate:

filament weight

filament cost

AMS purge waste

print time

electricity approximately

additional components

packaging

labor

failure allowance

total production cost

possible selling price

gross profit

gross margin.

If exact information is unavailable:

give an estimated range.

Clearly mark estimates.

---

# 16. PRINT TIME

Ideal:

under 2 hours.

Good:

2–4 hours.

Acceptable:

4–6 hours when margin is strong.

Avoid:

8+ hour products

unless selling price and profit are significantly higher.

Calculate:

PROFIT PER PRINTER HOUR.

This metric is critical.

A 100 MAD profit product taking 10 hours may be worse than a 40 MAD profit product taking 1 hour.

---

# 17. PROFIT PER PRINTER HOUR

Calculate:

Gross Profit ÷ Print Hours.

Rank products based partly on this metric.

My machine is my production capacity.

Therefore printer time is a limited resource.

---

# 18. BATCHABILITY

Evaluate whether I can place several products on one Bambu A1 plate.

Examples:

6 keychains

8 magnets

4 coasters

multiple tags.

Score:

BATCH PRODUCTION /10.

Products suitable for batch printing receive extra points.

---

# 19. PERSONALIZATION SPEED

Measure how long it takes to create a customer-specific version.

Ideal:

under 2 minutes.

Good:

under 5 minutes.

Bad:

15+ minutes of CAD work per customer.

Favor parametric/templates where only:

name

text

logo

number

or color

must be changed.

---

# 20. PRODUCT FAMILY SYSTEM

Do not recommend only individual objects.

Find PRODUCT SYSTEMS.

Example:

CUSTOM NAME COLLECTION

could contain:

keychain

desk sign

door sign

magnet

wall sign.

One design language can therefore create many SKUs.

This makes the business much easier.

---

# 21. NICHE RESEARCH

Generate at least:

30 possible 3D-printable niches/products internally.

Research them.

Then eliminate weak ones.

Give me only:

TOP 10 PRODUCT OPPORTUNITIES.

Then group them into:

TOP 3 BUSINESS NICHES.

---

# 22. NICHE REQUIREMENTS

A niche should support:

at least 5–10 products

personalization

different price levels

repeat orders or referrals

seasonal products

gift purchases

social media content

upsells

bundles.

Avoid niches dependent on one viral object.

---

# 23. MARKET SATURATION

Rate every product:

1 — almost absent

2 — emerging

3 — some competition

4 — competitive

5 — saturated.

I want mainly:

2–3.

A competitive product can still be recommended when we have a strong differentiation angle.

---

# 24. COMPETITOR ANALYSIS

Find actual Moroccan sellers when possible.

For each major candidate research:

product

price

customization

colors

delivery

presentation

reviews where available

quality

weaknesses.

Then answer:

HOW CAN WE MAKE OUR VERSION BETTER?

Examples:

better design

Arabic personalization

better color combinations

better packaging

premium photography

faster production

better size

Moroccan adaptation

bundle

gift packaging

business personalization.

---

# 25. ORIGINAL DESIGN VS DOWNLOADED MODEL

For every recommendation state:

A — DESIGN OURSELVES

B — GENERATOR/CUSTOMIZER

C — LICENSED EXISTING MODEL

Strong preference:

A or B.

This allows us to build a real business asset.

---

# 26. COMMERCIAL LICENSE CHECK

NEVER assume that a downloadable STL can legally be sold.

For every existing model:

check the commercial license.

Classify:

Commercial use allowed

Paid commercial license required

Personal use only

Unknown.

Reject:

Personal-use-only models

unless they are being used strictly as inspiration for a completely original design.

Also check:

copyright

trademarks

characters

sports logos

brands

movie characters

game characters.

Avoid relying on copyrighted characters or logos as the core business.

---

# 27. MODEL SOURCES

Search current trends on platforms such as:

MakerWorld

Printables

Cults3D

Thingiverse

MyMiniFactory

Thangs

Etsy physical products

Pinterest

and other relevant sources.

But use these primarily to discover:

trends

product formats

consumer demand

design ideas.

Do not blindly copy models.

---

# 28. BEST MODEL FORMAT

Prefer projects delivered as:

3MF

when Bambu-specific colors/plates/settings are important.

Also keep:

STL

for universal geometry.

When we create our own products, ideally maintain:

source CAD

+
STL

+
3MF.

---

# 29. FOUR-COLOR PRODUCT DESIGN

When creating product concepts, explicitly specify:

COLOR 1

COLOR 2

COLOR 3

COLOR 4

Example:

Base:
Matte black

Main text:
White

Accent:
Green

Small detail:
Red.

The design should still look attractive with:

2 colors

3 colors

or 4 colors.

---

# 30. MOROCCAN DESIGN LANGUAGE

Explore tasteful use of:

Moroccan geometric patterns

zellige-inspired geometry

Moroccan city silhouettes

Morocco map

Arabic typography

Darija expressions

Amazigh-inspired geometric aesthetics where appropriate

architecture

doors

arches

mosaics

local cultural references.

Do not create cheap souvenir-looking products automatically.

Look for:

modern Moroccan design.

---

# 31. THREE PRICE LEVELS

Try to build:

ENTRY PRODUCT

approximately low-cost impulse item.

CORE PRODUCT

medium-value personalized item.

PREMIUM PRODUCT

larger/high-value personalized product.

This creates a product ladder.

---

# 32. PRODUCTS TO AVOID

Strongly penalize:

support-heavy figurines

very tall thin models

large sculptures

models requiring extensive sanding

models requiring painting

fragile articulated products

extremely high polygon models

long 12–30 hour prints

models needing many screws

complex electronics

products using many purchased components

designs using more than four colors

products with excessive AMS changes

products requiring perfect tolerances

products where one failed print destroys a large amount of filament.

---

# 33. PRODUCT SCORING /100

Score each product:

Moroccan demand — 15

Profit potential — 15

Print reliability — 15

Print speed — 10

Perceived value — 10

Personalization — 10

Competition opportunity — 5

Four-color visual potential — 5

Batch production — 5

Ease of modeling — 5

Social media potential — 3

Expansion potential — 2

TOTAL = 100.

---

# 34. REQUIRED SCORE

Only seriously recommend products scoring:

75+/100.

Products:

85+ = Priority A+

80–84 = Priority A

75–79 = Test

below 75 = Reject.

---

# 35. BAMBU PRINTABILITY GATE

Before recommending ANY finalist, answer:

Can the A1 print it?

Does it fit the build plate?

How many colors?

Does AMS Lite handle it?

Does it need supports?

Expected print time?

Approximate filament?

How many color changes?

Purge waste?

Failure points?

Assembly?

Post-processing?

Can it batch print?

Is the 0.4 mm nozzle enough?

If ANY important answer is problematic:

reject or redesign the product.

---

# 36. REDESIGN INSTEAD OF REJECT

When an idea has good market potential but is too difficult to print:

attempt to redesign it.

For example:

complex sculpture
→ flat relief.

five colors
→ four colors.

many pieces
→ snap-fit two-piece design.

supports
→ split model.

large object
→ modular plates.

high-detail image
→ simplified geometric design.

Always search for the simplest manufacturable version.

---

# 37. OUTPUT FOR EACH FINAL PRODUCT

Provide:

PRODUCT NAME

NICHE

CUSTOMER

PROBLEM / PURPOSE

WHY PEOPLE BUY IT

MOROCCO DEMAND EVIDENCE

COMPETITORS

CURRENT MOROCCAN PRICE

OUR DIFFERENTIATION

PERSONALIZATION OPTIONS

COLORS

DIMENSIONS

MATERIAL

FILAMENT WEIGHT

PRINT TIME

NUMBER OF COLORS

AMS CHANGES

PURGE RISK

SUPPORTS

ASSEMBLY

POST-PROCESSING

BATCH QUANTITY PER PLATE

ESTIMATED COST

TARGET SELLING PRICE

ESTIMATED PROFIT

PROFIT / PRINT HOUR

PRINT DIFFICULTY /10

MARKET SCORE /100

FINAL VERDICT.

---

# 38. PROVIDE A MODEL CONCEPT

For every finalist describe exactly how the model should be built.

Example:

BASE

raised border

Arabic name

icon

back layer

keychain hole

dimensions

thickness

rounded corners

text height

color assignment.

The description should be detailed enough to recreate in:

Tinkercad

Fusion 360

FreeCAD

Onshape

or another CAD tool.

---

# 39. PROVIDE BAMBU STUDIO SETTINGS

For every finalist propose a starting profile:

Printer:
Bambu Lab A1

Nozzle:
0.4 mm

Material

Layer height

Walls

Top/bottom layers

Infill

Brim if needed

Supports

Orientation

AMS color assignment.

Use conservative settings optimized for:

reliability

quality

reasonable speed.

---

# 40. TEST PRINT

Before commercial production provide a:

TEST PRINT PLAN.

First create a small test if possible.

Check:

text

colors

bridging

fit

dimensions

surface quality

first layer.

Only then recommend full production.

---

# 41. TOP THREE BUSINESS DIRECTIONS

After researching everything, select:

NICHE A — BEST

NICHE B — SECOND

NICHE C — THIRD.

For each provide:

3 hero products

3 additional products

customer

price range

brand style

competition

market opportunity

Bambu compatibility.

---

# 42. FIRST PRODUCT TO PRINT

Finally choose:

ONE PRODUCT.

This should be the product with the best combination of:

market demand

profit

simplicity

speed

low filament use

easy personalization

low failure

strong visual result.

Give me:

exact model concept

size

colors

printing strategy

selling angle

estimated cost

target price

and a first prototype plan.

---

# 43. IMPORTANT RESEARCH PRINCIPLE

Do not ask:

“What is cool to 3D print?”

Ask:

“What product can one Bambu A1 manufacture reliably and repeatedly in Morocco while creating enough customer value to generate strong profit per printer hour?”

Manufacturing comes first.

Profitability second.

Novelty third.

Complexity last.

---

# FINAL OUTPUT

Create the final research as:

MOROCCO_BAMBU_3D_BUSINESS.md

Include:

# Executive Summary

# Morocco Market Research

# Competitor Research

# 30 Concepts Considered

# Concepts Rejected

# Top 10 Products

# Top 3 Niches

# Product Economics

# Bambu A1 Compatibility

# Printing Settings

# Commercial Licensing

# Product Development Roadmap

# First 5 Test Prints

# Final Recommendation

Finish with:

BEST NICHE:

BEST FIRST PRODUCT:

EXPECTED PRINT TIME:

EXPECTED FILAMENT:

COLORS:

ESTIMATED PRODUCTION COST:

TARGET PRICE:

ESTIMATED PROFIT:

PRINT DIFFICULTY:

WHY THIS SHOULD BE TESTED FIRST:

### One change I strongly recommend

Do **not** make “four colors” a requirement for every product. Make it a capability.

A beautiful black-and-white personalized product that takes 50 minutes and wastes almost no filament may be far more profitable than a four-color product requiring hundreds of AMS swaps.

So the business rule should be:

**Use 4 colors when they increase selling value, not simply because the printer supports 4 colors.**

And there is already a useful local benchmark: one Moroccan store is selling personalized keychains around **35 MAD** and small organizers around **79 MAD**, while another has moved into much higher-value Moroccan decorative pieces, including some around **690 MAD**. That tells us there is room to investigate both **high-volume personalized items** and **premium Moroccan-design objects** rather than competing only on cheap keychains. [To7fa](https://to7fa.ma/en?utm_source=chatgpt.com)

For your situation, my first research hypothesis would be **“Modern Personalized Moroccan Design”** rather than simply “3D printed gifts.” It gives you Arabic/French personalization, Moroccan identity, home/desk/business products, 1–4 colors, very easy A1 production, and much more room to build a recognizable brand.
Yes. I applied the direction to current Moroccan 3D-printing businesses and your **Bambu Lab A1 + AMS Lite**. The first result is quite clear: I would **not** start with complicated figurines. I would build around **fast personalized products with a Moroccan identity**, then expand into home/desk and B2B products.



## 🥇 Niche A — Personalized Moroccan Design

This is my current winner.

There is already evidence that Moroccan buyers understand this category. To7fa currently sells personalized name keychains around **35 MAD**, personalized name objects, party products, organizers, desk/gaming products, home décor, lamps and business products. It also offers COD and delivery across Morocco. [To7fa](https://to7fa.ma/en?utm_source=chatgpt.com)

The important part is that we **don't copy their catalog**. We make a recognizable design system specifically optimized for four-color Bambu printing.

Three hero products I would test:

| Product | Target price idea | A1 difficulty | Colors | Support | Why |
|---|---:|---:|---:|---|---|
| **Arabic/French Premium Name Keychain** | 39–59 MAD | 1/10 | 2–4 | None | Very cheap/fast test |
| **Personalized Desk/Room Name Sign** | 99–179 MAD | 2/10 | 2–4 | None | Higher perceived value |
| **Morocco Memory Map / City Sign** | 149–299 MAD | 3/10 | 2–4 | None | Premium/local identity |

The keychain shouldn't be a plain name. I would create a **three-layer visual system**: contrasting base, raised Arabic/French name, and optional icon/accent.

For example:

**Matte black base → ivory outline → red name → green accent**

or

**Sand → white → Majorelle blue → gold accent**

That creates something that looks branded rather than like a cheap single-color STL.

A parametric MakerWorld name-keychain design already demonstrates the manufacturing principle I want: customizable text, a flat base, raised second-color text, and **support-free printing**. [makerworld.bblmw.com](https://makerworld.bblmw.com/makerworld/model/US7b4942b9894239/design/25adddc52e146340.pdf?utm_source=chatgpt.com)

---

# 🥈 Niche B — Business Branding & Counter Products

I think this could actually become **more profitable than gifts** once you have customers.

Moroccan 3D-printing companies already advertise small-series manufacturing and customized objects with text/logos for businesses, which validates the general B2B need. [Impression 3D Maroc](https://3dprint.ma/?utm_source=chatgpt.com)

Three products:

| Product | Target price idea | Difficulty | Colors | Best customer |
|---|---:|---:|---:|---|
| QR + Instagram counter stand | 149–249 MAD | 2/10 | 2–3 | cafés, salons, shops |
| Custom company desk logo | 199–399 MAD | 2/10 | 2–4 | offices |
| Logo + name door/desk plaque | 149–299 MAD | 2/10 | 2–4 | professionals |

This niche is attractive because one customer can order **10, 20, 50 units**, rather than you acquiring a new customer for every 35 MAD keychain.

It is also extremely suitable for your A1.

Flat bases + extruded logos + text = reliable production.

---

# 🥉 Niche C — Modern Moroccan Home Décor

There is evidence of a much higher price ceiling here. 3DGIFI currently lists Moroccan heritage models in roughly the **590–790 MAD** range and also sells lighting, maps, custom busts and decorative products. [3DGIFI](https://3dgifi.ma/?utm_source=chatgpt.com)

I would simplify that idea dramatically for your single A1.

Instead of printing complicated monuments:

**3D monument → relief wall art**

**detailed mosque → architectural silhouette**

**complex city model → layered city map**

Your three products could be:

| Product | Target price idea | Difficulty | Colors | Typical print |
|---|---:|---:|---:|---:|
| Morocco layered wall map | 179–299 MAD | 2/10 | 3–4 | 2–4 h |
| Moroccan city skyline | 129–249 MAD | 2/10 | 2–3 | 1.5–3 h |
| Modern zellige wall tile set | 199–399 MAD | 3/10 | 3–4 | modular |

This is where your four-color AMS can create much more perceived value.

---

# Your machine is good enough

Your A1 has a **256 × 256 × 256 mm build volume** and an included **0.4 mm nozzle**. Bambu lists PLA and PETG among the ideal materials for it. [cdn1.bambulab.com](https://cdn1.bambulab.com/documentation/quick-start-a75adcb1d5d5e/Quick%20Start%20Guide%20for%20A1%20Combo.pdf?utm_source=chatgpt.com)

Your AMS Lite physically uses four filament paths/spools, so the design strategy above fits your current setup without requiring another machine. [cdn1.bambulab.com](https://cdn1.bambulab.com/documentation/quick-start-f507128172bdf/Quick%20start%20guide%20-%20A1%20combo-EN.pdf?utm_source=chatgpt.com)

More importantly, almost everything I'm proposing can be designed around:

**0.4 mm nozzle + PLA + 0.20 mm layers + no supports + flat printing.**

That's exactly what I want for your first commercial products.

---

# The product I would make first

### **Premium Arabic Name Keychain — Version 01**

Not because keychains are the ultimate business.

Because they are an excellent **manufacturing and market-learning product**.

Concept:

**65–85 mm width**

**3–4 mm total thickness**

Layer 1 — background  
Layer 2 — border  
Layer 3 — Arabic/French name  
Layer 4 — optional icon/accent

Example:

> **مريم**

White base  
Black border  
Majorelle-blue text  
Gold small star/heart/geometric accent

I would design it **flat on the bed, zero supports**.

A customizable commercial-use model indexed from MakerWorld has a reported print profile around **5–6 g and ~19 minutes**, demonstrating how economical this general product format can be; however, you should always re-check the original model's current commercial license before selling prints. [SliSearch](https://slisearch.com/en/models/a2835fdd-4161-4afc-9e40-ca4f725e8437?utm_source=chatgpt.com)

With your own design, licensing becomes much simpler.

---

# The bigger business model

Don't make the brand:

> **“I have a 3D printer and can print things.”**

Make it:

> **A Moroccan personalized-design brand that happens to manufacture with 3D printing.**

That difference is huge.

The customer shouldn't care that the machine is a Bambu A1.

They should care about:

**“I can get something beautiful with my name, my city, my story, my business or Moroccan identity.”**

And later your catalog can move naturally from:

**39 MAD → 99 MAD → 199 MAD → 399+ MAD**

instead of remaining trapped selling tiny prints.

---

# The website/workflow I recommend

For now:

**Tinkercad / Onshape → STL**

then

**Bambu Studio → 3MF → A1**

For personalized products, I would progressively replace manual editing with **parametric generators** where you enter:

`Name → font → dimensions → colors → generate model.`

That can eventually turn your website into something much more powerful:

Customer types:

> **Youssef / يوسف**

chooses:

> Black + White + Red

sees preview →

orders →

your system generates the production information →

you print it.

That's a much more defensible business than simply downloading popular STLs.

---

# My current ranking

**#1 Personalized Moroccan Design — 90/100**

Best balance of simplicity, personalization, low material usage, Moroccan relevance and product expansion.

**#2 Business Branding & Displays — 87/100**

Potentially the best profit/customer because of repeat and quantity orders.

**#3 Modern Moroccan Home Décor — 83/100**

Higher selling prices, but longer print times and therefore more production risk.

My recommended business would actually combine **#1 + #2 eventually under one design/manufacturing brand**, while keeping home décor as the premium collection.

The Moroccan market evidence supports this broader positioning: existing local businesses already sell personalized gifts and décor, custom manufacturing, business work and made-to-order pieces, so you're not trying to educate the market from zero. [3DGIFI](https://3dgifi.ma/contact-us/?utm_source=chatgpt.com)

**Next, the strongest move is to design the first 10 products specifically for the A1**—with dimensions, four-color layout, approximate print time/grams, target Morocco price, and a detailed AI/CAD prompt for generating each model.
# PROJECT HANDOFF — MOROCCO 3D PRINTING WEBSITE

I want you to continue this project as my coding/build agent.

## 1. PROJECT GOAL

Build a modern ecommerce website for a Morocco-based 3D-printing business using:

- Next.js
- React
- TypeScript
- Tailwind CSS
- mobile-first responsive design
- Arabic + French support later
- RTL-ready architecture
- fast loading
- clean premium branding
- simple ecommerce flow

Do NOT use Shopify.

The website should feel like a real Moroccan design brand, not like a generic 3D-printing or dropshipping site.

---

# 2. BUSINESS MODEL

I have:

- Bambu Lab A1
- AMS Lite
- up to 4 colors
- 0.4 mm nozzle
- PLA / PLA+ as main material
- PETG if required

The business will sell simple, reliable, repeatable 3D-printed products in Morocco.

The main idea is:

> Personalized Moroccan design products manufactured using 3D printing.

The customer should care about:

- personalization
- design
- Moroccan identity
- gift value
- business branding
- quality

—not the printer itself.

---

# 3. MAIN NICHE

Primary niche:

## Personalized Moroccan Design

The first product families should be:

### A. Personalized Gifts
Examples:

- Arabic name keychains
- French name keychains
- bilingual Arabic/French keychains
- personalized magnets
- small gift objects
- custom name pieces

### B. Home & Desk Personalization
Examples:

- desk name signs
- room/door signs
- personalized wall décor
- Morocco/city signs
- small organizers
- decorative name products

### C. Business Branding
Examples:

- QR-code stands
- Instagram stands
- custom company logo displays
- desk signs
- door signs
- counter displays
- business nameplates

Later:

### D. Modern Moroccan Home Décor
Examples:

- Morocco layered maps
- city skylines
- Moroccan geometric wall art
- zellige-inspired designs
- architectural silhouettes

---

# 4. PRODUCT DESIGN PHILOSOPHY

Products should be designed specifically for my Bambu Lab A1.

Prefer:

- maximum 4 colors
- ideally 2–3 colors
- flat-bottom designs
- no supports
- low print failure
- 0.4 mm nozzle compatible
- approximately 0.20 mm layer height
- low filament consumption
- simple geometry
- easy personalization
- easy batch printing
- high perceived value
- good profit per printer hour

Avoid:

- complicated figurines
- fragile articulated models
- large sculptures
- support-heavy models
- 8–20 hour prints
- designs requiring painting
- very detailed post-processing
- products needing many screws or parts
- products requiring more than 4 colors

---

# 5. FIRST HERO PRODUCT

The first prototype/product should be:

## Premium Personalized Arabic/French Name Keychain

Design direction:

- width around 65–85 mm
- total thickness around 3–4 mm
- flat print
- no supports
- customizable name
- Arabic or French
- optional bilingual version

Possible visual structure:

Layer 1:
background

Layer 2:
border

Layer 3:
raised name

Layer 4:
small icon/accent

Possible color examples:

### Option 1
- black
- white
- red
- green

### Option 2
- sand/beige
- white
- Majorelle blue
- gold/yellow

The model should remain attractive with only 2 colors too.

---

# 6. BRAND POSITIONING

Do NOT position the company as:

> “We own a 3D printer.”

Position it as:

> A modern Moroccan personalization and design brand.

Possible brand promise:

> Personalized objects inspired by your name, your story, your city, and Moroccan identity.

The brand should feel:

- modern
- Moroccan
- minimal
- creative
- premium
- trustworthy
- giftable
- Instagram-friendly

Avoid cheap souvenir aesthetics.

---

# 7. CUSTOMER TYPES

The website should eventually serve:

## Consumers

People buying:

- gifts
- personalized name objects
- home décor
- desk accessories
- wedding gifts
- birthday gifts
- Ramadan/Eid items
- custom products

## Businesses

Examples:

- cafés
- salons
- restaurants
- offices
- shops
- agencies
- small businesses

Products:

- QR signs
- logo displays
- desk branding
- counter stands
- custom signage

---

# 8. WEBSITE V1

Build a clean V1 first.

Main pages:

## Home

Sections:

1. Hero
2. Featured personalized products
3. How customization works
4. Product categories
5. Why choose us
6. Moroccan design section
7. Business/custom orders
8. Reviews/testimonials placeholder
9. FAQ
10. CTA
11. Footer

---

## Shop / Products

Grid of products.

Filters can be basic initially.

Categories:

- Personalized Gifts
- Desk & Home
- Business
- Moroccan Design

---

## Product Page

Each product should support:

- product images
- title
- price
- description
- personalization field
- name/text input
- color selector
- quantity
- optional size selector
- Add to Cart
- delivery information
- production time
- product details
- material
- dimensions
- FAQ
- related products

Important:

The personalization field should be a core feature.

Example:

Name to print:
[ Youssef ]

Language:
[ Arabic ] [ French ] [ Both ]

Colors:
[ color options ]

---

# 9. CART

Use a cart drawer rather than a full cart page if practical.

The drawer should show:

- product
- personalization
- color
- quantity
- price
- subtotal
- remove/edit
- continue shopping
- checkout CTA

---

# 10. CHECKOUT

For Morocco, start simple.

Initial checkout can be Cash on Delivery.

Collect:

- full name
- phone number
- city
- address
- optional note

Later payment integrations can be added.

Do not over-engineer payments in V1.

---

# 11. CUSTOM ORDER PAGE

Create:

## Custom Design / Request a Project

Customers can request:

- their name
- logo
- business sign
- custom decoration
- gift
- special object

Form:

- name
- phone
- city
- project type
- description
- quantity
- preferred colors
- optional image/logo upload

---

# 12. BUSINESS PAGE

Create a section/page for B2B.

Title idea:

## Solutions pour votre entreprise

Examples:

- QR stands
- logo displays
- nameplates
- counter signage
- personalized promotional products
- small series production

CTA:

> Request a quote

---

# 13. LANGUAGE

Start with French or French-first if it simplifies development.

But architecture must support:

- French
- Arabic
- RTL

Do not hardcode layout in a way that makes Arabic difficult later.

---

# 14. DESIGN SYSTEM

Use a premium minimalist visual language.

Avoid:

- overly colorful generic ecommerce
- childish 3D-printing aesthetic
- neon gaming style
- technical CAD-looking interface

Prefer:

- large product photos
- generous spacing
- neutral backgrounds
- one strong accent color
- elegant typography
- rounded cards/buttons
- clean mobile UX

The products should be the visual focus.

---

# 15. MOBILE FIRST

The majority of the website should work extremely well on mobile.

Prioritize:

- fast product browsing
- easy personalization
- large CTAs
- quick cart access
- very simple checkout
- minimal typing

---

# 16. DATA MODEL

Prepare a flexible product structure.

Each product should be able to contain:

```ts
id
slug
name
shortDescription
description
price
category
images
colors
sizes
material
dimensions
estimatedPrintTime
personalizable
personalizationOptions
featured
active
```

For orders:

```ts
id
customerName
phone
city
address
items
personalization
total
paymentMethod
orderStatus
createdAt
```

---

# 17. PRODUCT PERSONALIZATION

This is one of the most important technical parts.

Design the frontend so later we can connect it to a generator.

Future flow:

Customer enters:

Youssef

or:

يوسف

chooses:

- font
- size
- colors

and eventually sees a live preview.

Later we may automatically generate:

- STL
- 3MF
- production file
- order print instructions

Do NOT implement the full automatic CAD generation yet unless it is easy.

But structure the code so it can be added later.

---

# 18. FUTURE PRODUCTION AUTOMATION

Long-term idea:

Website order

→ personalization data

→ generation system

→ production file

→ Bambu Studio / print queue

→ Bambu A1

We may later generate models using:

- OpenSCAD
- CadQuery
- Fusion/parametric workflow
- another procedural model generator

Keep the architecture extensible.

---

# 19. PRODUCT PROFITABILITY

When adding products to the backend later, I want fields for internal production data:

```ts
filamentWeight
estimatedFilamentCost
printHours
numberOfColors
supportRequired
estimatedProductionCost
sellingPrice
profitEstimate
profitPerPrinterHour
```

These fields do NOT have to appear publicly.

They are for internal business management.

---

# 20. INITIAL PRODUCTS

Create placeholder/demo data for these products:

### Product 1
Premium Personalized Name Keychain

### Product 2
Personalized Desk Name Sign

### Product 3
Morocco / City Decorative Sign

### Product 4
Business QR Code Stand

### Product 5
Company Logo Desk Display

### Product 6
Personalized Door/Room Sign

Use realistic placeholder content but do not invent customer reviews.

---

# 21. PRICE PLACEHOLDERS

For initial frontend mockup we can use approximate ranges:

Keychains:
39–59 MAD

Small personalized products:
79–129 MAD

Desk signs:
99–179 MAD

Business signs:
149–299 MAD

Premium décor:
179–399+ MAD

These are placeholders and should be easy to change.

---

# 22. SEO

Prepare SEO-friendly pages.

Important possible search concepts:

- cadeau personnalisé Maroc
- cadeau 3D Maroc
- porte clé personnalisé Maroc
- cadeau prénom arabe
- décoration personnalisée Maroc
- impression 3D Maroc
- plaque personnalisée Maroc
- enseigne QR Maroc
- cadeau entreprise Maroc

Do not keyword-stuff.

---

# 23. TECH STACK

Preferred:

Next.js latest stable version

React

TypeScript

Tailwind CSS

App Router

Use reusable components.

Keep dependencies minimal.

Use local/mock data initially.

Avoid unnecessary backend complexity in the first version.

---

# 24. CODE QUALITY

I want:

- clean folder structure
- reusable components
- strong TypeScript types
- responsive layout
- good accessibility
- semantic HTML
- loading/error handling
- easy future expansion

Do not put the entire project into giant components.

---

# 25. INITIAL PROJECT STRUCTURE

Suggested:

```txt
app/
  page.tsx
  shop/
  product/[slug]/
  custom/
  business/
  contact/
  checkout/

components/
  layout/
  product/
  cart/
  personalization/
  ui/

data/
  products.ts

types/
  product.ts
  order.ts

lib/
```

Improve this structure if you have a better architecture.

---

# 26. FIRST DEVELOPMENT MILESTONE

Do not try to build everything at once.

Start by delivering:

### Milestone 1

- project setup
- global design system
- header
- footer
- homepage
- shop grid
- product card
- one complete product page
- personalization UI
- responsive mobile design
- mock product data

Then continue with:

### Milestone 2

- cart drawer
- checkout
- custom order page
- business page

Then:

### Milestone 3

- backend/order storage
- production management
- admin
- automatic model generation

---

# 27. IMPORTANT

Do not start by creating a complicated backend.

The first objective is:

> Build a beautiful working ecommerce frontend that proves the brand and shopping experience.

The website needs to feel good enough that a Moroccan customer would trust it as a real brand.

---

# 28. FIRST TASK

Start now with Milestone 1.

Before coding, briefly state:

1. proposed architecture
2. design direction
3. component structure
4. route structure

Then implement it.

Make sensible decisions yourself instead of asking me many questions.

When a choice is reversible, choose the simplest high-quality option and continue.
````

## Fichier lib/brand.ts

```typescript
export const brand = {
  name: 'MustDesign3D',
  location: 'Maroc',
  tagline: 'Des objets qui parlent de vous.',
  email: process.env.NEXT_PUBLIC_CONTACT_EMAIL ?? '',
  phone: process.env.NEXT_PUBLIC_CONTACT_PHONE ?? '',
  whatsapp: process.env.NEXT_PUBLIC_CONTACT_WHATSAPP ?? '',
};

export function contactLinks() {
  const links: { label: string; href: string }[] = [];
  if (/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(brand.email)) links.push({ label: brand.email, href: `mailto:${brand.email}` });
  if (/^\+[1-9]\d{7,14}$/.test(brand.phone)) links.push({ label: brand.phone, href: `tel:${brand.phone}` });
  if (/^\+[1-9]\d{7,14}$/.test(brand.whatsapp)) links.push({ label: 'WhatsApp', href: `https://wa.me/${brand.whatsapp.slice(1)}` });
  return links;
}

export const labels = { demo: 'Démo locale · commandes bientôt disponibles', cart: 'Panier', shop: 'Boutique', custom: 'Sur mesure', business: 'Professionnels', contact: 'Contact', indicative: 'Prix indicatif', preview: 'Illustration originale · démo 2D' };
```

## Fichier lib/cart-storage.ts

```typescript
import type { CartLine, Product } from './contracts';
import { isQuantity, isRecord, optionKey, validatePersonalization } from './validation';

export const CART_STORAGE_KEY = 'mustdesign3d.cart';
export type CartRestore = { lines: CartLine[]; notices: string[]; persistent: boolean };

export function restoreCart(raw: string | null, products: Product[]): CartRestore {
  const result: CartRestore = { lines: [], notices: [], persistent: true };
  if (raw === null) return result;
  try {
    const stored: unknown = JSON.parse(raw);
    if (!isRecord(stored) || stored.schemaVersion !== 1 || !Array.isArray(stored.lines) || stored.lines.length > 100) {
      return { lines: [], notices: ['Version du panier non prise en charge. Un nouveau panier en mémoire est disponible.'], persistent: false };
    }
    for (const candidate of stored.lines) {
      if (!isRecord(candidate)) { result.notices.push('Une ligne de panier endommagée a été ignorée.'); continue; }
      const product = products.find(item => item.id === candidate.productId);
      if (!product) { result.notices.push('Un produit retiré du catalogue a été écarté du panier.'); continue; }
      if (product.pricingMode === 'quote' || product.priceCents === null) {
        result.notices.push('Un article passé sur devis a été retiré du panier. Son projet peut être préparé depuis la fiche.');
        continue;
      }
      const legacyPalettes: Record<string, string> = { 'sable-majorelle': 'bleu-blanc', 'foret-ivoire': 'noir-blanc', 'argile-charbon': 'rouge-blanc' };
      let options = candidate.personalization;
      if (isRecord(options) && typeof options.paletteId === 'string' && Object.hasOwn(legacyPalettes, options.paletteId)) {
        options = { ...options, paletteId: product.personalizationSchema.kind === 'qr' ? 'blanc-noir' : legacyPalettes[options.paletteId] };
        result.notices.push('Une ancienne palette a été adaptée aux filaments bleu, noir, blanc et rouge. Vérifiez les couleurs de votre composition.');
      }
      if (product.personalizationSchema.kind === 'qr' && isRecord(options) && options.kind === 'qr'
        && !Object.hasOwn(options, 'businessName') && !Object.hasOwn(options, 'destinationType')) {
        options = { ...options, businessName: 'À compléter', destinationType: 'menu' };
        result.notices.push('Une ancienne composition QR a été mise à jour. Remplacez le nom provisoire lors de sa modification.');
      }
      const personalization = validatePersonalization(product, options);
      if (!personalization || personalization.kind === 'none' || !isQuantity(candidate.quantity) || typeof candidate.id !== 'string' || !/^[a-zA-Z0-9-]{1,80}$/.test(candidate.id)) {
        result.notices.push('Des options ou une quantité indisponibles ont été écartées du panier.'); continue;
      }
      if (candidate.unitPriceCents !== product.priceCents) result.notices.push('Les prix indicatifs ont été actualisés selon le catalogue.');
      const equivalent = result.lines.find(line => optionKey(line.productId, line.personalization) === optionKey(product.id, personalization));
      if (equivalent) {
        const quantity = equivalent.quantity + candidate.quantity;
        if (quantity > 99) result.notices.push('Un doublon dépassant 99 exemplaires a été écarté.');
        else equivalent.quantity = quantity;
      } else if (result.lines.some(line => line.id === candidate.id)) result.notices.push('Une ligne avec un identifiant dupliqué a été écartée.');
      else result.lines.push({ id: candidate.id, productId: product.id, personalization, quantity: candidate.quantity, unitPriceCents: product.priceCents });
    }
    result.notices = [...new Set(result.notices)];
    return result;
  } catch {
    return { lines: [], notices: ['Panier enregistré illisible. Vous pouvez continuer avec un panier en mémoire.'], persistent: false };
  }
}
```

## Fichier lib/catalogue.server.ts

```typescript
import 'server-only';
import type { Palette, Product } from './contracts';

const palettes: Palette[] = [
  { id: 'bleu-blanc', label: 'Bleu · Blanc', colors: ['#233d99', '#fafafa'] },
  { id: 'noir-blanc', label: 'Noir · Blanc', colors: ['#161616', '#fafafa'] },
  { id: 'blanc-noir', label: 'Blanc · Noir', colors: ['#fafafa', '#161616'] },
  { id: 'rouge-blanc', label: 'Rouge · Blanc', colors: ['#b92b32', '#fafafa'] },
];

type Definition = Omit<Product, 'currency' | 'images' | 'status' | 'material' | 'palettes' | 'pricingMode' | 'visibility'> & {
  pricingMode?: Product['pricingMode'];
  visibility?: Product['visibility'];
};

const definitions: Definition[] = [
  {
    id: 'md-keychain-01', slug: 'porte-cles-prenom', name: 'Porte-clés prénom',
    categoryId: 'cadeaux', priceCents: 4900, featured: true, mark: 'مريم',
    shortDescription: 'Votre prénom, à emporter partout.',
    description: 'Composez un petit cadeau à votre nom, en français, en arabe ou avec les deux graphies. La forme et la solidité de l’œillet seront confirmées sur le prototype.',
    dimensionsMm: { width: 75, depth: 28, height: 4 },
    personalizationSchema: { kind: 'name', maxGraphemes: 24 },
  },
  {
    id: 'md-desk-01', slug: 'plaque-bureau', name: 'Plaque de bureau',
    categoryId: 'maison-bureau', priceCents: 9900, featured: true, mark: 'Yasmine',
    shortDescription: 'Un nom. Une place à vous.',
    description: 'Votre nom ou votre fonction en relief sur une plaque à poser. Choisissez une palette et préparez la composition qui accompagnera votre espace de travail.',
    dimensionsMm: { width: 160, depth: 45, height: 55 },
    personalizationSchema: { kind: 'text', label: 'Nom ou fonction', placeholder: 'Yasmine · Architecte', maxGraphemes: 40 },
  },
  {
    id: 'md-door-01', slug: 'plaque-porte', name: 'Plaque de porte',
    categoryId: 'maison-bureau', priceCents: 9900, featured: false, mark: 'L’atelier',
    shortDescription: 'Le début de votre univers.',
    description: 'Une plaque personnalisée pour une pièce, une famille ou un atelier. Les dimensions, les perçages et la tenue de la fixation seront vérifiés avant fabrication.',
    dimensionsMm: { width: 150, depth: 65, height: 4 },
    personalizationSchema: { kind: 'text', label: 'Texte de la plaque', placeholder: 'L’atelier de Lina', maxGraphemes: 32 },
  },
  {
    id: 'md-qr-01', slug: 'support-qr', name: 'Présentoir QR',
    categoryId: 'professionnels', priceCents: 14900, featured: true, mark: 'Votre menu',
    shortDescription: 'Un lien, à portée de téléphone.',
    description: 'Présentez un menu, une page ou un lien professionnel sur votre comptoir. Le QR est généré localement depuis votre lien HTTPS. Le code imprimé et la stabilité du support restent à tester sur prototype.',
    dimensionsMm: { width: 90, depth: 55, height: 125 },
    personalizationSchema: { kind: 'qr', maxLength: 2048 },
  },
  {
    id: 'md-plate-01', slug: 'porte-cles-plaque-marocaine', name: 'Porte-clés plaque marocaine',
    categoryId: 'cadeaux', priceCents: 4500, featured: false, mark: '12345 | أ | 6',
    shortDescription: 'Une petite touche de chez vous.',
    description: 'Préparez votre composition de plaque miniature en saisissant le numéro, la lettre et le code souhaités, séparés par des traits. L’atelier vérifiera la disposition sur le modèle.',
    dimensionsMm: { width: 70, depth: 20, height: 4 },
    personalizationSchema: { kind: 'text', label: 'Numéro · lettre · code', placeholder: '12345 | أ | 6', maxGraphemes: 24 },
  },
  {
    id: 'md-bag-01', slug: 'etiquette-sac', name: 'Étiquette de sac',
    categoryId: 'cadeaux', priceCents: 3900, featured: false, mark: 'Lina',
    shortDescription: 'Votre sac porte votre signature.',
    description: 'Un prénom lisible sur une étiquette plate à accrocher. La forme de l’attache sera validée avant fabrication. Choisissez le texte et deux couleurs pour votre aperçu.',
    dimensionsMm: { width: 85, depth: 32, height: 3 },
    personalizationSchema: { kind: 'text', label: 'Prénom de l’étiquette', placeholder: 'Lina', maxGraphemes: 24 },
  },
  {
    id: 'md-place-01', slug: 'marque-places-personnalises', name: 'Marque-places personnalisés',
    categoryId: 'cadeaux', priceCents: null, pricingMode: 'quote', featured: false, mark: 'Nour',
    shortDescription: 'Une attention pour chaque invité.',
    description: 'Une série de dix prénoms pour une table ou un événement. Préparez la liste et le thème de votre projet. Le prix du lot dépendra des noms et des dimensions validés.',
    dimensionsMm: null, personalizationSchema: { kind: 'none', bespoke: true },
  },
  {
    id: 'md-contact-01', slug: 'plaque-contact', name: 'Plaque de contact',
    categoryId: 'professionnels', priceCents: 9900, featured: false, mark: '@votre.atelier',
    shortDescription: 'Votre nom, au bon endroit.',
    description: 'Une enseigne compacte pour indiquer votre activité et votre identifiant social. La composition définitive et son système de pose se préparent après validation du prototype.',
    dimensionsMm: { width: 140, depth: 80, height: 4 },
    personalizationSchema: { kind: 'text', label: 'Nom ou identifiant à afficher', placeholder: '@votre.atelier', maxGraphemes: 40 },
  },
  {
    id: 'md-logo-batch-01', slug: 'porte-cles-logo-lot', name: 'Porte-clés logo en lot',
    categoryId: 'professionnels', priceCents: null, pricingMode: 'quote', featured: false, mark: 'MD',
    shortDescription: 'Votre marque, en petite série.',
    description: 'Préparez un visuel dont vous détenez les droits et la quantité souhaitée. La simplification du logo, le prix unitaire et le montant du lot seront étudiés ensemble.',
    dimensionsMm: null, personalizationSchema: { kind: 'none', bespoke: true },
  },
  {
    id: 'md-city-01', slug: 'ville-maroc', name: 'Décoration ville du Maroc',
    categoryId: 'decoration', priceCents: 19900, visibility: 'prototype', featured: false, mark: 'Marrakech',
    shortDescription: 'Une étude de silhouette marocaine.',
    description: 'Ce concept original explore des arches et volumes géométriques. Il reste dans l’espace des prototypes en attendant une validation de sa forme et de sa fabrication.',
    dimensionsMm: { width: 180, depth: 35, height: 95 },
    personalizationSchema: { kind: 'text', label: 'Votre ville', placeholder: 'Marrakech', maxGraphemes: 32 },
  },
  {
    id: 'md-logo-01', slug: 'logo-bureau', name: 'Logo de bureau',
    categoryId: 'professionnels', priceCents: null, pricingMode: 'quote', visibility: 'prototype', featured: false, mark: 'MD',
    shortDescription: 'Une étude pour votre identité.',
    description: 'Ce gabarit de présentoir est un point de départ pour un projet de logo. Votre forme, ses droits et sa stabilité seront étudiés avant toute fabrication.',
    dimensionsMm: null, personalizationSchema: { kind: 'none', bespoke: true },
  },
  {
    id: 'md-pixel-01', slug: 'plaque-pixel-zellige', name: 'Plaque pixel Zellige',
    categoryId: 'decoration', priceCents: 11900, visibility: 'prototype', featured: false, mark: 'Zellige',
    shortDescription: 'Une étude de motif en relief.',
    description: 'Ce prototype original explore un motif pixel en trois couleurs. Il reste dans la galerie technique pour préparer une future collection de décoration.',
    dimensionsMm: { width: 86, depth: 86, height: 3.6 },
    personalizationSchema: { kind: 'none', bespoke: true },
  },
];

const renderedSlugs = new Set(['porte-cles-prenom', 'plaque-bureau', 'plaque-porte', 'support-qr', 'ville-maroc', 'logo-bureau', 'plaque-pixel-zellige']);

const catalogue: Product[] = definitions.map(entry => ({
  ...entry,
  pricingMode: entry.pricingMode ?? 'fixed',
  visibility: entry.visibility ?? 'shop',
  currency: 'MAD',
  status: 'demo',
  material: 'PLA · fabrication à valider',
  images: renderedSlugs.has(entry.slug) ? [{
    src: '/models/' + entry.slug + '.png',
    alt: 'Vue du prototype OpenSCAD ' + entry.name,
    isDemo: true,
    kind: 'cad-preview',
    modelVersion: '1',
  }] : [],
  palettes: entry.id === 'md-qr-01' ? palettes.filter(palette => palette.id === 'blanc-noir') : palettes,
}));

function toPublicProduct(product: Product): Product {
  return {
    id: product.id, slug: product.slug, name: product.name,
    shortDescription: product.shortDescription, description: product.description,
    categoryId: product.categoryId, priceCents: product.priceCents,
    pricingMode: product.pricingMode, visibility: product.visibility,
    currency: product.currency, status: product.status, material: product.material,
    images: product.images.map(image => ({ ...image })),
    dimensionsMm: product.dimensionsMm ? { ...product.dimensionsMm } : null,
    palettes: product.palettes.map(palette => ({ ...palette, colors: [...palette.colors] })),
    personalizationSchema: { ...product.personalizationSchema }, mark: product.mark,
    featured: product.featured,
  };
}

export const getAllProducts = (): Product[] => catalogue.map(toPublicProduct);
export const getProducts = (): Product[] => getAllProducts().filter(product => product.visibility === 'shop');
export const getModelProducts = (): Product[] => getAllProducts().filter(product => product.images.some(image => image.kind === 'cad-preview'));
export const getProductBySlug = (slug: string): Product | undefined => getAllProducts().find(product => product.slug === slug);
```

## Fichier lib/contracts.ts

```typescript
export type CategoryId = 'cadeaux' | 'maison-bureau' | 'professionnels' | 'decoration';
export type QrDestinationType = 'menu' | 'website' | 'social' | 'reviews' | 'other';
export type Palette = { id: string; label: string; colors: string[] };
export type ProductImage = { src: string; alt: string; isDemo: boolean; kind?: 'photo' | 'generated-concept' | 'cad-preview'; modelVersion?: string };
export type DimensionsMm = { width: number; depth: number; height: number };
export type PersonalizationSchema =
  | { kind: 'name'; maxGraphemes: number }
  | { kind: 'text'; label: string; placeholder: string; maxGraphemes: number }
  | { kind: 'qr'; maxLength: number }
  | { kind: 'none'; bespoke: true };
export type Product = {
  id: string;
  slug: string;
  name: string;
  shortDescription: string;
  description: string;
  categoryId: CategoryId;
  priceCents: number | null;
  pricingMode: 'fixed' | 'quote';
  visibility: 'shop' | 'prototype';
  currency: 'MAD';
  images: ProductImage[];
  mark: string;
  featured: boolean;
  status: 'demo' | 'draft' | 'active' | 'archived';
  material: string;
  dimensionsMm: DimensionsMm | null;
  palettes: Palette[];
  personalizationSchema: PersonalizationSchema;
};
export type Personalization =
  | { version: 1; kind: 'name'; language: 'fr' | 'ar' | 'both'; frenchName: string | null; arabicName: string | null; paletteId: string }
  | { version: 1; kind: 'text'; text: string; paletteId: string }
  | { version: 1; kind: 'qr'; businessName: string; destinationType: QrDestinationType; url: string; paletteId: string }
  | { version: 1; kind: 'none' };
export type CartLine = { id: string; productId: string; personalization: Personalization; quantity: number; unitPriceCents: number };
export type StoredCart = { schemaVersion: 1; lines: CartLine[] };
export type Customer = { name: string; phone: string; city: string; address: string };
export type OrderRequest = { items: Pick<CartLine, 'productId' | 'quantity' | 'personalization'>[]; customer: Customer; note?: string };
export type OrderItem = { productId: string; productNameSnapshot: string; quantity: number; unitPriceCents: number; personalizationSnapshot: Personalization; lineTotalCents: number };
export type Order = { id: string; reference: string; customer: Customer; items: OrderItem[]; subtotalCents: number; shippingCents: number; totalCents: number; currency: 'MAD'; paymentMethod: 'cod'; status: 'pending' | 'confirmed' | 'cancelled'; createdAt: string };
export type Quote = { id: string; reference: string; name: string; phone: string; city: string; projectType: 'sign' | 'logo' | 'series' | 'other'; description: string; quantity: number; requestedPalette: string; status: 'pending' | 'reviewed' | 'closed'; createdAt: string };
export type ApiError = { error: { code: 'DEMO_MODE'; message: string } };
```

## Fichier lib/internal-contracts.ts

```typescript
import 'server-only';
import type { DimensionsMm } from './contracts';

export type SourceObservation = { id: string; sourceSite: string; externalId: string | null; sourceUrl: string; originalUrl: string | null; observedAt: string; observationStatus: 'observed' | 'unavailable'; notes: string };
export type ModelRecord = { id: string; sourceObservationId: string | null; creator: string; licenceLabel: string; licenceUrl: string | null; permissions: { commercialPrint: boolean | null; modify: boolean | null; redistribute: boolean | null }; reviewStatus: 'needs_review' | 'approved' | 'rejected'; rightsEvidenceRef: string };
export type ModelAsset = { id: string; modelId: string; version: number; format: 'scad' | 'stl' | '3mf'; privateStorageKey: string; sha256: string; acquiredAt: string };
export type ManufacturingData = { productId: string; modelAssetId: string | null; material: string; dimensionsMm: DimensionsMm | null; filamentGrams: number | null; purgeGrams: number | null; printHours: number | null; colorCount: number; supportRequired: boolean | null; productionCostCents: number | null; slicedAt: string | null; prototypeStatus: 'unvalidated' | 'validated' };
export type RightsReview = { modelId: string; reviewer: string; reviewedAt: string; commercialPrintEvidence: string | null; modificationEvidence: string | null; redistributionEvidence: string | null; mediaEvidence: string | null };
```

## Fichier lib/mode.server.ts

```typescript
import 'server-only';
import type { ApiError } from './contracts';

export function getOperatingMode() {
  const demoRequested = process.env.DEMO_MODE !== 'false';
  return { isDemo: true as const, demoRequested, writesEnabled: false as const };
}

export function rejectUnavailableWrite() {
  getOperatingMode();
  const body: ApiError = { error: { code: 'DEMO_MODE', message: 'Commandes bientôt disponibles. Aucune donnée reçue ni enregistrée.' } };
  return Response.json(body, { status: 403, headers: { 'Cache-Control': 'no-store' } });
}
```

## Fichier lib/products.ts

```typescript
export type { Product, Palette, Personalization, CartLine } from './contracts';

export const collections = [
  { id: 'cadeaux', label: 'Cadeaux personnalisés', note: 'Un petit objet, une vraie attention.' },
  { id: 'maison-bureau', label: 'Maison & bureau', note: 'Votre place, votre signature.' },
  { id: 'professionnels', label: 'Professionnels', note: 'Les détails qui vous distinguent.' },
] as const;

export const categoryLabel = (id: string) => collections.find(collection => collection.id === id)?.label ?? id;
export const formatPrice = (cents: number) => new Intl.NumberFormat('fr-MA', { style: 'currency', currency: 'MAD', maximumFractionDigits: 2 }).format(cents / 100);
export const normalizeSearch = (value: string) => value.toLocaleLowerCase('fr').normalize('NFD').replace(/\p{M}/gu, '');

export const filamentColors = [
  { id: 'white', label: 'Blanc', hex: '#fafafa' },
  { id: 'black', label: 'Noir', hex: '#161616' },
  { id: 'blue', label: 'Bleu', hex: '#233d99' },
  { id: 'red', label: 'Rouge', hex: '#b92b32' },
] as const;

export function productPrice(product: import('./contracts').Product) {
  return product.pricingMode === 'quote' || product.priceCents === null ? 'Sur devis' : formatPrice(product.priceCents);
}
```

## Fichier lib/validation.ts

```typescript
import type { Personalization, Product, QrDestinationType } from './contracts';

export const graphemeCount = (value: string) => Array.from(new Intl.Segmenter('fr', { granularity: 'grapheme' }).segment(value.trim())).length;
export const isQuantity = (value: unknown): value is number => typeof value === 'number' && Number.isInteger(value) && value >= 1 && value <= 99;
export const isRecord = (value: unknown): value is Record<string, unknown> => typeof value === 'object' && value !== null && !Array.isArray(value);
const exactKeys = (value: Record<string, unknown>, keys: string[]) => Object.keys(value).length === keys.length && keys.every(key => Object.hasOwn(value, key));
const validText = (value: unknown, maximum: number): value is string => typeof value === 'string' && !/[\u0000-\u001f\u007f\u202a-\u202e\u2066-\u2069]/u.test(value) && graphemeCount(value) >= 1 && graphemeCount(value) <= maximum;
const qrDestinationTypes: QrDestinationType[] = ['menu', 'website', 'social', 'reviews', 'other'];

export function textError(value: string, maximum: number): string | undefined {
  return validText(value, maximum) ? undefined : `Saisissez de 1 à ${maximum} caractères visibles, sans saut de ligne.`;
}

export function isHttpsUrl(value: unknown): value is string {
  if (typeof value !== 'string' || value.length > 2048 || /\s/u.test(value)) return false;
  try {
    const url = new URL(value);
    return url.protocol === 'https:' && !!url.hostname && !url.username && !url.password;
  } catch { return false; }
}

export function validatePersonalization(product: Product, value: unknown): Personalization | null {
  if (!isRecord(value) || value.version !== 1 || value.kind !== product.personalizationSchema.kind) return null;
  if (value.kind === 'none') return exactKeys(value, ['version', 'kind']) ? { version: 1, kind: 'none' } : null;
  if (!product.palettes.some(palette => palette.id === value.paletteId)) return null;
  const paletteId = value.paletteId as string;
  if (value.kind === 'name' && product.personalizationSchema.kind === 'name') {
    if (!exactKeys(value, ['version', 'kind', 'language', 'frenchName', 'arabicName', 'paletteId'])) return null;
    const maximum = product.personalizationSchema.maxGraphemes;
    const language = value.language;
    if (language !== 'fr' && language !== 'ar' && language !== 'both') return null;
    if (language === 'ar' ? value.frenchName !== null : !validText(value.frenchName, maximum)) return null;
    if (language === 'fr' ? value.arabicName !== null : !validText(value.arabicName, maximum)) return null;
    return { version: 1, kind: 'name', language, frenchName: typeof value.frenchName === 'string' ? value.frenchName.trim() : null, arabicName: typeof value.arabicName === 'string' ? value.arabicName.trim() : null, paletteId };
  }
  if (value.kind === 'text' && product.personalizationSchema.kind === 'text' && exactKeys(value, ['version', 'kind', 'text', 'paletteId']) && validText(value.text, product.personalizationSchema.maxGraphemes)) {
    return { version: 1, kind: 'text', text: value.text.trim(), paletteId };
  }
  if (value.kind === 'qr' && exactKeys(value, ['version', 'kind', 'businessName', 'destinationType', 'url', 'paletteId'])
    && validText(value.businessName, 32) && qrDestinationTypes.includes(value.destinationType as QrDestinationType) && isHttpsUrl(value.url)) {
    return { version: 1, kind: 'qr', businessName: value.businessName.trim(), destinationType: value.destinationType as QrDestinationType, url: value.url, paletteId };
  }
  return null;
}

export function personalizationLabel(value: Personalization): string[] {
  if (value.kind === 'name') return [value.frenchName, value.arabicName].filter((name): name is string => name !== null);
  if (value.kind === 'text') return [value.text];
  if (value.kind === 'qr') {
    const destinations: Record<QrDestinationType, string> = { menu: 'Menu ou carte', website: 'Site web', social: 'Réseau social', reviews: 'Avis clients', other: 'Autre page' };
    return ['Établissement : ' + value.businessName, 'Destination : ' + destinations[value.destinationType], value.url];
  }
  return ['Étude sur mesure'];
}

export const optionKey = (productId: string, value: Personalization) => JSON.stringify([productId, value]);
```

## Fichier next.config.ts

```typescript
import type { NextConfig } from 'next';

const config: NextConfig = { turbopack: { root: process.cwd() }, outputFileTracingRoot: process.cwd() };

export default config;
```

## Fichier package-lock.json

```json
{
  "name": "atelier-prenom",
  "version": "0.1.0",
  "lockfileVersion": 3,
  "requires": true,
  "packages": {
    "": {
      "name": "atelier-prenom",
      "version": "0.1.0",
      "dependencies": {
        "next": "16.4.6",
        "qrcode": "^1.5.4",
        "react": "19",
        "react-dom": "19"
      },
      "devDependencies": {
        "@tailwindcss/postcss": "4.3.5",
        "@types/node": "^22",
        "@types/qrcode": "^1.5.6",
        "@types/react": "^19",
        "@types/react-dom": "^19",
        "tailwindcss": "4.3.5",
        "typescript": "^5"
      },
      "engines": {
        "node": "22.x"
      }
    },
    "node_modules/@alloc/quick-lru": {
      "version": "5.3.0",
      "resolved": "https://registry.npmjs.org/@alloc/quick-lru/-/quick-lru-5.3.0.tgz",
      "integrity": "sha512-U4+70Pc5ZS9osnCBCE5Jha/ciHM+Yp+CNMNC/7HvYbNRk1Ldd+f7qO65W5qfhu/TCv+/ozljlXXe9Nj8419DMA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/@emnapi/runtime": {
      "version": "1.11.3",
      "resolved": "https://registry.npmjs.org/@emnapi/runtime/-/runtime-1.11.3.tgz",
      "integrity": "sha512-Xz4Tpyki7XyrpbUK1jR1AhdAdaXyhhY4lZ3neLodmhpuWfy2PAQN5B46sAiU4liOXGLkHypn/qU+jvfWSCYYLA==",
      "license": "MIT",
      "optional": true,
      "dependencies": {
        "tslib": "^2.4.0"
      }
    },
    "node_modules/@img/colour": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/@img/colour/-/colour-1.1.0.tgz",
      "integrity": "sha512-Td76q7j57o/tLVdgS746cYARfSyxk8iEfRxewL9h4OMzYhbW4TAcppl0mT4eyqXddh6L/jwoM75mo7ixa/pCeQ==",
      "license": "MIT",
      "optional": true,
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@img/sharp-darwin-arm64": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-darwin-arm64/-/sharp-darwin-arm64-0.35.5.tgz",
      "integrity": "sha512-QRUlFQ0WxvdWyqqG/WtI3iupfD5rBzmCHXSdPsY91sAtVtTo7Q4cb6zOccZ3gqEqkr0f1As1ehLqmEpDsRf+lg==",
      "cpu": [
        "arm64"
      ],
      "license": "Apache-2.0",
      "optional": true,
      "os": [
        "darwin"
      ],
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      },
      "optionalDependencies": {
        "@img/sharp-libvips-darwin-arm64": "1.3.4"
      }
    },
    "node_modules/@img/sharp-darwin-x64": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-darwin-x64/-/sharp-darwin-x64-0.35.5.tgz",
      "integrity": "sha512-+BR255RhDlpygUpOc/Jdt1nT6DQ3XG/ERo5wbcdOf5Q320dKtPCKPLR1LJs9VGXRaMa8l1uUa0tkCNOXiAxZUw==",
      "cpu": [
        "x64"
      ],
      "license": "Apache-2.0",
      "optional": true,
      "os": [
        "darwin"
      ],
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      },
      "optionalDependencies": {
        "@img/sharp-libvips-darwin-x64": "1.3.4"
      }
    },
    "node_modules/@img/sharp-freebsd-wasm32": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-freebsd-wasm32/-/sharp-freebsd-wasm32-0.35.5.tgz",
      "integrity": "sha512-Y/z91nEZ4uIBX5X3nfTovjU9lHNKFYbL2lpHCLVNmXQK03VIZvXBBt0KxbPGp2SdGSF+2mQU4e+hQaWOt86iAw==",
      "license": "Apache-2.0",
      "optional": true,
      "os": [
        "freebsd"
      ],
      "dependencies": {
        "@img/sharp-wasm32": "0.35.5"
      },
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-libvips-darwin-arm64": {
      "version": "1.3.4",
      "resolved": "https://registry.npmjs.org/@img/sharp-libvips-darwin-arm64/-/sharp-libvips-darwin-arm64-1.3.4.tgz",
      "integrity": "sha512-5R89nBYiRdUlSWJxPhO+GVtaXzXSxKnRu/xqMn3KTA3L9EB9Oy/P+Nn2f2vlhPuUdy/Zusb2DarbyTpGCfEDuw==",
      "cpu": [
        "arm64"
      ],
      "license": "LGPL-3.0-or-later",
      "optional": true,
      "os": [
        "darwin"
      ],
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-libvips-darwin-x64": {
      "version": "1.3.4",
      "resolved": "https://registry.npmjs.org/@img/sharp-libvips-darwin-x64/-/sharp-libvips-darwin-x64-1.3.4.tgz",
      "integrity": "sha512-iR2OKH80yi0U+dUplyh3/xdpFvps6YkCwsXenIJxqxR1v9o+xtKTGbS9H7cps+2Vxjc8B1j96p75NmTGjIhtpQ==",
      "cpu": [
        "x64"
      ],
      "license": "LGPL-3.0-or-later",
      "optional": true,
      "os": [
        "darwin"
      ],
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-libvips-linux-arm": {
      "version": "1.3.4",
      "resolved": "https://registry.npmjs.org/@img/sharp-libvips-linux-arm/-/sharp-libvips-linux-arm-1.3.4.tgz",
      "integrity": "sha512-LmRtTsOHuvM2+wlO2Db37dx5MiZhB0FvSunciw48YjdOkZz9KAiRbm8ujeMOA1INqmei5NapFxYEK1D1ZSidmw==",
      "cpu": [
        "arm"
      ],
      "libc": [
        "glibc"
      ],
      "license": "LGPL-3.0-or-later",
      "optional": true,
      "os": [
        "linux"
      ],
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-libvips-linux-arm64": {
      "version": "1.3.4",
      "resolved": "https://registry.npmjs.org/@img/sharp-libvips-linux-arm64/-/sharp-libvips-linux-arm64-1.3.4.tgz",
      "integrity": "sha512-Y3dgX/6lE2QhQb+Gxy0WZxfg9MEm/JBjamZpS2IklP7xIQoKN4hzAm7KcMVGtaVDt3neE9OKBC7vAfonA/Lr1A==",
      "cpu": [
        "arm64"
      ],
      "libc": [
        "glibc"
      ],
      "license": "LGPL-3.0-or-later",
      "optional": true,
      "os": [
        "linux"
      ],
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-libvips-linux-ppc64": {
      "version": "1.3.4",
      "resolved": "https://registry.npmjs.org/@img/sharp-libvips-linux-ppc64/-/sharp-libvips-linux-ppc64-1.3.4.tgz",
      "integrity": "sha512-Le6boB8Tai0Nis+gIxIpKx68UDVVIqdR8Tin5Yf1z2LJJQLDJvCDRqRu+jC2qCoD+eIomonmOwB4smBRxfVpYQ==",
      "cpu": [
        "ppc64"
      ],
      "libc": [
        "glibc"
      ],
      "license": "LGPL-3.0-or-later",
      "optional": true,
      "os": [
        "linux"
      ],
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-libvips-linux-riscv64": {
      "version": "1.3.4",
      "resolved": "https://registry.npmjs.org/@img/sharp-libvips-linux-riscv64/-/sharp-libvips-linux-riscv64-1.3.4.tgz",
      "integrity": "sha512-aHkkIEHPRdQEegJN20MLmGtxYD9R2wQr3Cwpddnu5+YKMt6Uzax7S9h5gpZTo8wyrGuZSlfQ63OevL5mTyOC7Q==",
      "cpu": [
        "riscv64"
      ],
      "libc": [
        "glibc"
      ],
      "license": "LGPL-3.0-or-later",
      "optional": true,
      "os": [
        "linux"
      ],
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-libvips-linux-s390x": {
      "version": "1.3.4",
      "resolved": "https://registry.npmjs.org/@img/sharp-libvips-linux-s390x/-/sharp-libvips-linux-s390x-1.3.4.tgz",
      "integrity": "sha512-ra/mB6MikESDUO7Yg+Mi95bFBb9GsObURuhnOv3OqknjGe9sZrG8tCe9q0xSIGrtLgvgw0gKnFWcK4blSgQOuQ==",
      "cpu": [
        "s390x"
      ],
      "libc": [
        "glibc"
      ],
      "license": "LGPL-3.0-or-later",
      "optional": true,
      "os": [
        "linux"
      ],
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-libvips-linux-x64": {
      "version": "1.3.4",
      "resolved": "https://registry.npmjs.org/@img/sharp-libvips-linux-x64/-/sharp-libvips-linux-x64-1.3.4.tgz",
      "integrity": "sha512-GJ//SSXbnwSDes02umB3nDJLFcQzw8a18V8fyhqr6tV515tOEMdImjjxj1AoafMRz56F3PHgftnj1QEKSU1zkw==",
      "cpu": [
        "x64"
      ],
      "libc": [
        "glibc"
      ],
      "license": "LGPL-3.0-or-later",
      "optional": true,
      "os": [
        "linux"
      ],
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-libvips-linuxmusl-arm64": {
      "version": "1.3.4",
      "resolved": "https://registry.npmjs.org/@img/sharp-libvips-linuxmusl-arm64/-/sharp-libvips-linuxmusl-arm64-1.3.4.tgz",
      "integrity": "sha512-hvulFwtjUcagsis6BBxHwGFwWoNZjgYmULGVrZcyfNbjA8hKILbRxGg15/7w5HDyXHXUos/j6baAWqnCyQ2DWA==",
      "cpu": [
        "arm64"
      ],
      "libc": [
        "musl"
      ],
      "license": "LGPL-3.0-or-later",
      "optional": true,
      "os": [
        "linux"
      ],
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-libvips-linuxmusl-x64": {
      "version": "1.3.4",
      "resolved": "https://registry.npmjs.org/@img/sharp-libvips-linuxmusl-x64/-/sharp-libvips-linuxmusl-x64-1.3.4.tgz",
      "integrity": "sha512-6zXKeE/p39I1AmA3cJG35eyBGNqNddLnUXjhwBnsGjFPWqf5VKkDBEqaEkPDoTEtkxwi2vv8Tcr2mDyP4So7Fg==",
      "cpu": [
        "x64"
      ],
      "libc": [
        "musl"
      ],
      "license": "LGPL-3.0-or-later",
      "optional": true,
      "os": [
        "linux"
      ],
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-linux-arm": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-linux-arm/-/sharp-linux-arm-0.35.5.tgz",
      "integrity": "sha512-LEaXK2WdXVK5ykcw0buWyPMsmLLL2vpHLD6yrNSW+JGEL3BZPA4tpKN6iaMc4AxTTAoaX/sU1rOL51lcIz48ZQ==",
      "cpu": [
        "arm"
      ],
      "libc": [
        "glibc"
      ],
      "license": "Apache-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      },
      "optionalDependencies": {
        "@img/sharp-libvips-linux-arm": "1.3.4"
      }
    },
    "node_modules/@img/sharp-linux-arm64": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-linux-arm64/-/sharp-linux-arm64-0.35.5.tgz",
      "integrity": "sha512-LYVx5JTsOM2CBzmxreh+nl64/3H6Xb09iSLknqH47z2T2DFFxDeFLP5y4dJwe6H7uGQlHPyEEtIqyo3DYsRwdQ==",
      "cpu": [
        "arm64"
      ],
      "libc": [
        "glibc"
      ],
      "license": "Apache-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      },
      "optionalDependencies": {
        "@img/sharp-libvips-linux-arm64": "1.3.4"
      }
    },
    "node_modules/@img/sharp-linux-ppc64": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-linux-ppc64/-/sharp-linux-ppc64-0.35.5.tgz",
      "integrity": "sha512-QVxAAq8evVRI9ia2vqgwrmWucn5Dfv+JdWzj75pD8omHLPSP7f8p20O8jxzjCcuCEQEOtYOZUmX1hkiZ0kdevA==",
      "cpu": [
        "ppc64"
      ],
      "libc": [
        "glibc"
      ],
      "license": "Apache-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      },
      "optionalDependencies": {
        "@img/sharp-libvips-linux-ppc64": "1.3.4"
      }
    },
    "node_modules/@img/sharp-linux-riscv64": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-linux-riscv64/-/sharp-linux-riscv64-0.35.5.tgz",
      "integrity": "sha512-LtdreXguaavKODPIfzJ4kffx7UNt1omwtK0rch4EBbbSTXPnxWmYSayXdLJw0fJzQ97kHt1gL/yh4tvU+nCyRQ==",
      "cpu": [
        "riscv64"
      ],
      "libc": [
        "glibc"
      ],
      "license": "Apache-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      },
      "optionalDependencies": {
        "@img/sharp-libvips-linux-riscv64": "1.3.4"
      }
    },
    "node_modules/@img/sharp-linux-s390x": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-linux-s390x/-/sharp-linux-s390x-0.35.5.tgz",
      "integrity": "sha512-UZasTOFiYzotTsGOCu42BfUzP6Tu6Do/947iRm1RsLKvlllxwGcn4RN27LibGWceix4Y+Pmw3jsnTcCQIgWjqA==",
      "cpu": [
        "s390x"
      ],
      "libc": [
        "glibc"
      ],
      "license": "Apache-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      },
      "optionalDependencies": {
        "@img/sharp-libvips-linux-s390x": "1.3.4"
      }
    },
    "node_modules/@img/sharp-linux-x64": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-linux-x64/-/sharp-linux-x64-0.35.5.tgz",
      "integrity": "sha512-SxFtLTeJInhAA9Q836kux2vZNeOBQEx658qvbboZScr0wIARym3IcGmW7KpVD5sbVg0Ojy+udFQdayYIZyoNog==",
      "cpu": [
        "x64"
      ],
      "libc": [
        "glibc"
      ],
      "license": "Apache-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      },
      "optionalDependencies": {
        "@img/sharp-libvips-linux-x64": "1.3.4"
      }
    },
    "node_modules/@img/sharp-linuxmusl-arm64": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-linuxmusl-arm64/-/sharp-linuxmusl-arm64-0.35.5.tgz",
      "integrity": "sha512-9HbMclmI1zlNkFRs3z9/eBtDjfD0sGlrX1z6b1qwmiFY5ElDLh4BC0LPBdVp7z1DXFiKlIcznf+ZlsuZzLxQqg==",
      "cpu": [
        "arm64"
      ],
      "libc": [
        "musl"
      ],
      "license": "Apache-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      },
      "optionalDependencies": {
        "@img/sharp-libvips-linuxmusl-arm64": "1.3.4"
      }
    },
    "node_modules/@img/sharp-linuxmusl-x64": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-linuxmusl-x64/-/sharp-linuxmusl-x64-0.35.5.tgz",
      "integrity": "sha512-4KOphqB035HrVdqLZfCgMzzERrQkkzOwRhl4OAkRO1YCldbaFjySXMaK534Mo0V+LndnlJk+sbUyLeU0ULyD1A==",
      "cpu": [
        "x64"
      ],
      "libc": [
        "musl"
      ],
      "license": "Apache-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      },
      "optionalDependencies": {
        "@img/sharp-libvips-linuxmusl-x64": "1.3.4"
      }
    },
    "node_modules/@img/sharp-wasm32": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-wasm32/-/sharp-wasm32-0.35.5.tgz",
      "integrity": "sha512-Ptsga1su4tQx+LLF1ECS9U6nz5kmrXKo6XVbtR48Ke3ZRxxgaWBu7IDtEe1quo8hiupwm6WFqxVlXaSf7IINGQ==",
      "license": "Apache-2.0 AND LGPL-3.0-or-later AND MIT",
      "optional": true,
      "dependencies": {
        "@emnapi/runtime": "^1.11.3"
      },
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-webcontainers-wasm32": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-webcontainers-wasm32/-/sharp-webcontainers-wasm32-0.35.5.tgz",
      "integrity": "sha512-hfhF/FmoQyTUkA0bIKFOtw536BQSeBMe6BF6QyWlrPxT754+TFLaZ7sKKTfvvM0yJgKgaYTwnFCIZ/GuDw5SUA==",
      "cpu": [
        "wasm32"
      ],
      "license": "Apache-2.0",
      "optional": true,
      "dependencies": {
        "@img/sharp-wasm32": "0.35.5"
      },
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-win32-arm64": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-win32-arm64/-/sharp-win32-arm64-0.35.5.tgz",
      "integrity": "sha512-X4t7g+7ZA5DKblCBEXGjUqqemj4vczING/5viFwAL8h4N3qYeyjwdCvRLHi4EdOUI+2Z7UFlp1VM+p/AuEtm6Q==",
      "cpu": [
        "arm64"
      ],
      "license": "Apache-2.0 AND LGPL-3.0-or-later",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-win32-ia32": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-win32-ia32/-/sharp-win32-ia32-0.35.5.tgz",
      "integrity": "sha512-5Zm82LoBc43nhwNybZlG7Y1KO//Zhsn306fQl29ZOuStHLGTo3BWL83q3cznX0poxSAMuYL1On/BHBxkBeKr6A==",
      "cpu": [
        "ia32"
      ],
      "license": "Apache-2.0 AND LGPL-3.0-or-later",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": "^20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@img/sharp-win32-x64": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/@img/sharp-win32-x64/-/sharp-win32-x64-0.35.5.tgz",
      "integrity": "sha512-x76eH0vEiHlcMQu8Y8IenntaACtddpT6W0wmXtWrnKcnKI7ME5DdgqhAD6SEWOEl1v2zDvkZDhFA9KnURwpfqg==",
      "cpu": [
        "x64"
      ],
      "license": "Apache-2.0 AND LGPL-3.0-or-later",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      }
    },
    "node_modules/@jridgewell/gen-mapping": {
      "version": "0.3.13",
      "resolved": "https://registry.npmjs.org/@jridgewell/gen-mapping/-/gen-mapping-0.3.13.tgz",
      "integrity": "sha512-2kkt/7niJ6MgEPxF0bYdQ6etZaA+fQvDcLKckhy1yIQOzaoKjBBjSj63/aLVjYE3qhRt5dvM+uUyfCg6UKCBbA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@jridgewell/sourcemap-codec": "^1.5.0",
        "@jridgewell/trace-mapping": "^0.3.24"
      }
    },
    "node_modules/@jridgewell/remapping": {
      "version": "2.3.5",
      "resolved": "https://registry.npmjs.org/@jridgewell/remapping/-/remapping-2.3.5.tgz",
      "integrity": "sha512-LI9u/+laYG4Ds1TDKSJW2YPrIlcVYOwi2fUC6xB43lueCjgxV4lffOCZCtYFiH6TNOX+tQKXx97T4IKHbhyHEQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@jridgewell/gen-mapping": "^0.3.5",
        "@jridgewell/trace-mapping": "^0.3.24"
      }
    },
    "node_modules/@jridgewell/resolve-uri": {
      "version": "3.1.2",
      "resolved": "https://registry.npmjs.org/@jridgewell/resolve-uri/-/resolve-uri-3.1.2.tgz",
      "integrity": "sha512-bRISgCIjP20/tbWSPWMEi54QVPRZExkuD9lJL+UIxUKtwVJA8wW1Trb1jMs1RFXo1CBTNZ/5hpC9QvmKWdopKw==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=6.0.0"
      }
    },
    "node_modules/@jridgewell/sourcemap-codec": {
      "version": "1.6.0",
      "resolved": "https://registry.npmjs.org/@jridgewell/sourcemap-codec/-/sourcemap-codec-1.6.0.tgz",
      "integrity": "sha512-T7jf+5zgsZHwNJ4lvQ7/aezbyk0nNX+zJVWpmHA7VYsEx7a7qr5Rg5IbtJFqkgze5Y2sruq1RUY8Q837Od7iFw==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/@jridgewell/trace-mapping": {
      "version": "0.3.31",
      "resolved": "https://registry.npmjs.org/@jridgewell/trace-mapping/-/trace-mapping-0.3.31.tgz",
      "integrity": "sha512-zzNR+SdQSDJzc8joaeP8QQoCQr8NuYx2dIIytl1QeBEZHJ9uW6hebsrYgbz8hJwUQao3TWCMtmfV8Nu1twOLAw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@jridgewell/resolve-uri": "^3.1.0",
        "@jridgewell/sourcemap-codec": "^1.4.14"
      }
    },
    "node_modules/@next/env": {
      "version": "16.4.6",
      "resolved": "https://registry.npmjs.org/@next/env/-/env-16.4.6.tgz",
      "integrity": "sha512-SunBjJ6t+oBtecS3dTjdVuMhUogP5wD/vrGL5EVuQYM1iS4O5ilL51HkiJ3sPjMzRHiCChvr4dbaSJbR7F3lxA==",
      "license": "MIT"
    },
    "node_modules/@next/swc-darwin-arm64": {
      "version": "16.4.6",
      "resolved": "https://registry.npmjs.org/@next/swc-darwin-arm64/-/swc-darwin-arm64-16.4.6.tgz",
      "integrity": "sha512-kJ4VVZkley17xKaJx72QN2IBqjrj7zenCQZaUF0l9ShS/1Mt2kW4+Z5KGG6vgr3L/J562xTOizVyM1iA/u5nlg==",
      "cpu": [
        "arm64"
      ],
      "license": "MIT",
      "optional": true,
      "os": [
        "darwin"
      ],
      "engines": {
        "node": ">= 10"
      }
    },
    "node_modules/@next/swc-darwin-x64": {
      "version": "16.4.6",
      "resolved": "https://registry.npmjs.org/@next/swc-darwin-x64/-/swc-darwin-x64-16.4.6.tgz",
      "integrity": "sha512-eIPGZIqC+8JKaeZmvnCANJQF4xWkkHqSnAAajtFxgwDMAOnCgxNvP52SeWZ41PyVwoe+Le/NQuZSaQ8j7YshSA==",
      "cpu": [
        "x64"
      ],
      "license": "MIT",
      "optional": true,
      "os": [
        "darwin"
      ],
      "engines": {
        "node": ">= 10"
      }
    },
    "node_modules/@next/swc-linux-arm64-gnu": {
      "version": "16.4.6",
      "resolved": "https://registry.npmjs.org/@next/swc-linux-arm64-gnu/-/swc-linux-arm64-gnu-16.4.6.tgz",
      "integrity": "sha512-9nI6O8vvczH2D9ZNdMGqb/3NuT15T9ksOZnAmx9/gjF2cOi74+xxyf1Hk96uIMfm14c9y6wHeBq6SH8g6udvcA==",
      "cpu": [
        "arm64"
      ],
      "libc": [
        "glibc"
      ],
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 10"
      }
    },
    "node_modules/@next/swc-linux-arm64-musl": {
      "version": "16.4.6",
      "resolved": "https://registry.npmjs.org/@next/swc-linux-arm64-musl/-/swc-linux-arm64-musl-16.4.6.tgz",
      "integrity": "sha512-7/qPhTxDp2ScluOJOhLuhWmlA17o1yZ0SIgpISBCpBxXgtnK4+KGywBpFkfLPiU1rnSM1faFGzYkH6i7JdTrqA==",
      "cpu": [
        "arm64"
      ],
      "libc": [
        "musl"
      ],
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 10"
      }
    },
    "node_modules/@next/swc-linux-x64-gnu": {
      "version": "16.4.6",
      "resolved": "https://registry.npmjs.org/@next/swc-linux-x64-gnu/-/swc-linux-x64-gnu-16.4.6.tgz",
      "integrity": "sha512-oOpbNa8XOW1qCGd9VvzC4fbkkRxEls7/WI6tz+YHC0xRA7KpV1U7DrAnCPjzVyOk/karzWEepCOcTIDmwK8FwQ==",
      "cpu": [
        "x64"
      ],
      "libc": [
        "glibc"
      ],
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 10"
      }
    },
    "node_modules/@next/swc-linux-x64-musl": {
      "version": "16.4.6",
      "resolved": "https://registry.npmjs.org/@next/swc-linux-x64-musl/-/swc-linux-x64-musl-16.4.6.tgz",
      "integrity": "sha512-aM8CZ+OR2EwXaAYw7KGkW2GDmNDsLBIRe1MMRZCJPTdw/xhTD0IMUVO4sf3KqrzuRouGzwwLZn34+gFeVXiUQA==",
      "cpu": [
        "x64"
      ],
      "libc": [
        "musl"
      ],
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 10"
      }
    },
    "node_modules/@next/swc-win32-arm64-msvc": {
      "version": "16.4.6",
      "resolved": "https://registry.npmjs.org/@next/swc-win32-arm64-msvc/-/swc-win32-arm64-msvc-16.4.6.tgz",
      "integrity": "sha512-U0p7/tEtqvHX2crhd841CDwKtp5CFkKXVjOhmfccR3Pvp64sj8KBwRqsvltqLOwVBbj0NtkxwXSDpEHYGbxeXQ==",
      "cpu": [
        "arm64"
      ],
      "license": "MIT",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">= 10"
      }
    },
    "node_modules/@next/swc-win32-x64-msvc": {
      "version": "16.4.6",
      "resolved": "https://registry.npmjs.org/@next/swc-win32-x64-msvc/-/swc-win32-x64-msvc-16.4.6.tgz",
      "integrity": "sha512-3ZG15/5WIdlTQsIEvc9sPTTSL5XFrlLklIKmfF4fwsDnoAhu6NcBDXsk3mbGxNyo6aVLEGex+fHCv2MahY7a9g==",
      "cpu": [
        "x64"
      ],
      "license": "MIT",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">= 10"
      }
    },
    "node_modules/@swc/helpers": {
      "version": "0.5.23",
      "resolved": "https://registry.npmjs.org/@swc/helpers/-/helpers-0.5.23.tgz",
      "integrity": "sha512-5lSsMOTXURePglDfvuAQUqkGek9Hg2kksOYay2m0+XR++b2NWYL/4sWyuvVBIs8oKnJaxkdi9whaL/sqN13afw==",
      "license": "Apache-2.0",
      "dependencies": {
        "tslib": "^2.8.0"
      }
    },
    "node_modules/@tailwindcss/node": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/node/-/node-4.3.5.tgz",
      "integrity": "sha512-yT53FzV4ke0cr/BguDxhWMpm5MJu1O2muzk+tKw6lKHjODAsYArBbWwFbJiaksfzFv1tpkO9QHGzmfs1hJT66g==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@jridgewell/remapping": "^2.3.5",
        "enhanced-resolve": "^5.24.5",
        "jiti": "^2.7.0",
        "lightningcss": "1.33.0",
        "magic-string": "^1.1.0",
        "source-map-js": "^1.2.1",
        "tailwindcss": "4.3.5"
      }
    },
    "node_modules/@tailwindcss/oxide": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/oxide/-/oxide-4.3.5.tgz",
      "integrity": "sha512-PynqGLZsZvwM9tqD/CUxkOIfyd6K5elZ2MooauzJryP/UqXYgi3yYbtt3N0Xe+MHV/eFKPFQCEfIKAqlAS1CBg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 20"
      },
      "optionalDependencies": {
        "@tailwindcss/oxide-android-arm64": "4.3.5",
        "@tailwindcss/oxide-darwin-arm64": "4.3.5",
        "@tailwindcss/oxide-darwin-x64": "4.3.5",
        "@tailwindcss/oxide-freebsd-x64": "4.3.5",
        "@tailwindcss/oxide-linux-arm-gnueabihf": "4.3.5",
        "@tailwindcss/oxide-linux-arm64-gnu": "4.3.5",
        "@tailwindcss/oxide-linux-arm64-musl": "4.3.5",
        "@tailwindcss/oxide-linux-x64-gnu": "4.3.5",
        "@tailwindcss/oxide-linux-x64-musl": "4.3.5",
        "@tailwindcss/oxide-wasm32-wasi": "4.3.5",
        "@tailwindcss/oxide-win32-arm64-msvc": "4.3.5",
        "@tailwindcss/oxide-win32-x64-msvc": "4.3.5"
      }
    },
    "node_modules/@tailwindcss/oxide-android-arm64": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/oxide-android-arm64/-/oxide-android-arm64-4.3.5.tgz",
      "integrity": "sha512-Se0z5xMqcSQanJD1IYmO0cGpK3iv0fp3ZsIT7xRJZ1Da5PghvNoc46zz4jIQn+aan3dV9T8AermFNN9QPmsh0Q==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "android"
      ],
      "engines": {
        "node": ">= 20"
      }
    },
    "node_modules/@tailwindcss/oxide-darwin-arm64": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/oxide-darwin-arm64/-/oxide-darwin-arm64-4.3.5.tgz",
      "integrity": "sha512-UPrgTDuUbvmqGMZuCnmI3FKee/tYKzKdp00/kuB4oSGB213VYg8QTdF7lVhnPoBXq/mIfJ+ILoBFqNOboWcMwQ==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "darwin"
      ],
      "engines": {
        "node": ">= 20"
      }
    },
    "node_modules/@tailwindcss/oxide-darwin-x64": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/oxide-darwin-x64/-/oxide-darwin-x64-4.3.5.tgz",
      "integrity": "sha512-E+p7HEtjI0b8D7kbbWxH067cGui6d4c79COGko9fAPVE3rwc1E7ld2HFCbaG86AOGWS5VKQYqZOaf38ya4uxTQ==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "darwin"
      ],
      "engines": {
        "node": ">= 20"
      }
    },
    "node_modules/@tailwindcss/oxide-freebsd-x64": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/oxide-freebsd-x64/-/oxide-freebsd-x64-4.3.5.tgz",
      "integrity": "sha512-yWEWcWyAG7rWOcTpJTjdhQ3pcaFY2h+0bqTRfgU3G2fz87ZU3AKdvdZKhslD+kyHnjBUWKvNdRYwIYC5dI1tIg==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "freebsd"
      ],
      "engines": {
        "node": ">= 20"
      }
    },
    "node_modules/@tailwindcss/oxide-linux-arm-gnueabihf": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/oxide-linux-arm-gnueabihf/-/oxide-linux-arm-gnueabihf-4.3.5.tgz",
      "integrity": "sha512-WmeVjtJhZlr+smpqcdR2kQkkn6arHIJnUIBxTO2EJcTLGY1ecVXNo2hbSn8xc0IH2aEtys936iMWKGyj0GaKnA==",
      "cpu": [
        "arm"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 20"
      }
    },
    "node_modules/@tailwindcss/oxide-linux-arm64-gnu": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/oxide-linux-arm64-gnu/-/oxide-linux-arm64-gnu-4.3.5.tgz",
      "integrity": "sha512-DTCSyucc6ShMp1QMqV5R94Z7xlgNgUzkGmFF1rL5HH2Qjy4eSmEqy+YLGkqqYvWa4sILtgrBt1JjRKbneQtiFQ==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "libc": [
        "glibc"
      ],
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 20"
      }
    },
    "node_modules/@tailwindcss/oxide-linux-arm64-musl": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/oxide-linux-arm64-musl/-/oxide-linux-arm64-musl-4.3.5.tgz",
      "integrity": "sha512-H9lsvO4x9E4nE4Hi8h7NHHw0O/kcVSu+iOyFHNGdYzazGgDjFHZbE6S3hQ8kMcbNXSBlMdNi67LV5EVqtpaJtw==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "libc": [
        "musl"
      ],
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 20"
      }
    },
    "node_modules/@tailwindcss/oxide-linux-x64-gnu": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/oxide-linux-x64-gnu/-/oxide-linux-x64-gnu-4.3.5.tgz",
      "integrity": "sha512-4uxQvtBvPuIdl13WfUBj9xMZHH14PtHZ8OZdtLmdyDtG66sCa1t599NZT+jagkUzRtWhuul1qRZQ1nAJscXN5g==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "libc": [
        "glibc"
      ],
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 20"
      }
    },
    "node_modules/@tailwindcss/oxide-linux-x64-musl": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/oxide-linux-x64-musl/-/oxide-linux-x64-musl-4.3.5.tgz",
      "integrity": "sha512-0JQAzs7jwbA7O6+z/adU+Jk3AXwsu3npAhtr5escXS7TqEqWcaDV7qHuI+0Vy/KQRuVGnLQREcSJWYauyV3oqg==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "libc": [
        "musl"
      ],
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 20"
      }
    },
    "node_modules/@tailwindcss/oxide-wasm32-wasi": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/oxide-wasm32-wasi/-/oxide-wasm32-wasi-4.3.5.tgz",
      "integrity": "sha512-OJhFmlEfdzMr+avACdi40RPtnkW0B6hXyxL/8r+tnEHBWZji36CYRjEXrrvgBmaYsD3oEOBqwYFRKsYvzFe7Bw==",
      "bundleDependencies": [
        "@napi-rs/wasm-runtime",
        "@emnapi/core",
        "@emnapi/runtime",
        "@tybys/wasm-util",
        "@emnapi/wasi-threads",
        "tslib"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "dependencies": {
        "@emnapi/core": "^1.11.3",
        "@emnapi/runtime": "^1.11.3",
        "@emnapi/wasi-threads": "^1.2.3",
        "@napi-rs/wasm-runtime": "^1.2.2",
        "@tybys/wasm-util": "^0.10.3",
        "tslib": "^2.8.1"
      },
      "engines": {
        "node": "^20.19.0 || ^22.13.0 || >=23.5.0"
      }
    },
    "node_modules/@tailwindcss/oxide-wasm32-wasi/node_modules/@emnapi/core": {
      "version": "1.11.3",
      "dev": true,
      "inBundle": true,
      "license": "MIT",
      "optional": true,
      "dependencies": {
        "@emnapi/wasi-threads": "1.2.3",
        "tslib": "^2.4.0"
      }
    },
    "node_modules/@tailwindcss/oxide-wasm32-wasi/node_modules/@emnapi/runtime": {
      "version": "1.11.3",
      "dev": true,
      "inBundle": true,
      "license": "MIT",
      "optional": true,
      "dependencies": {
        "tslib": "^2.4.0"
      }
    },
    "node_modules/@tailwindcss/oxide-wasm32-wasi/node_modules/@emnapi/wasi-threads": {
      "version": "1.2.3",
      "dev": true,
      "inBundle": true,
      "license": "MIT",
      "optional": true,
      "dependencies": {
        "tslib": "^2.4.0"
      }
    },
    "node_modules/@tailwindcss/oxide-wasm32-wasi/node_modules/@napi-rs/wasm-runtime": {
      "version": "1.2.2",
      "dev": true,
      "inBundle": true,
      "license": "MIT",
      "optional": true,
      "dependencies": {
        "@tybys/wasm-util": "^0.10.3"
      },
      "engines": {
        "node": "^20.19.0 || ^22.13.0 || >=23.5.0"
      },
      "funding": {
        "type": "github",
        "url": "https://github.com/sponsors/Brooooooklyn"
      },
      "peerDependencies": {
        "@emnapi/core": "^1.7.1 || ^2.0.0-alpha.3",
        "@emnapi/runtime": "^1.7.1 || ^2.0.0-alpha.3"
      }
    },
    "node_modules/@tailwindcss/oxide-wasm32-wasi/node_modules/@tybys/wasm-util": {
      "version": "0.10.3",
      "dev": true,
      "inBundle": true,
      "license": "MIT",
      "optional": true,
      "dependencies": {
        "tslib": "^2.4.0"
      }
    },
    "node_modules/@tailwindcss/oxide-wasm32-wasi/node_modules/tslib": {
      "version": "2.8.1",
      "dev": true,
      "inBundle": true,
      "license": "0BSD",
      "optional": true
    },
    "node_modules/@tailwindcss/oxide-win32-arm64-msvc": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/oxide-win32-arm64-msvc/-/oxide-win32-arm64-msvc-4.3.5.tgz",
      "integrity": "sha512-9o8jgthi+QE5eandnboiJT64VQfnIArfZzSTdgbhEK5aafdiu2jTW9Honi/mwYHxBZuH1vAC57IFyrh+0iK5Gg==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">= 20"
      }
    },
    "node_modules/@tailwindcss/oxide-win32-x64-msvc": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/oxide-win32-x64-msvc/-/oxide-win32-x64-msvc-4.3.5.tgz",
      "integrity": "sha512-XiKFfIy1RWe7qK4WqByxNW7Oz1/nkOy8o/BWhHminyV1PmpUd8Eedj5v2A8h2kpqeVlz6xRnwk9Fr/ZXNLcZfg==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">= 20"
      }
    },
    "node_modules/@tailwindcss/postcss": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@tailwindcss/postcss/-/postcss-4.3.5.tgz",
      "integrity": "sha512-FAV37Tlx9wBiT/hkfgVD0Q6CWsP2oUX3lf28nrfjW8+ksILjnpuFulUqWDfNR4/ZiEHHDRBX8DUTzD1Rys687A==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@alloc/quick-lru": "^5.2.0",
        "@tailwindcss/node": "4.3.5",
        "@tailwindcss/oxide": "4.3.5",
        "postcss": "^8.5.25",
        "tailwindcss": "4.3.5"
      }
    },
    "node_modules/@types/node": {
      "version": "22.20.5",
      "resolved": "https://registry.npmjs.org/@types/node/-/node-22.20.5.tgz",
      "integrity": "sha512-U2+DNr+wSjpsTS/wZGYHq7GcwfuSmKiKvoPvK22zwTlRhU91yOniN4qRR5KhIjvif7ysw/dz/hKmfDH0Ris4aA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "undici-types": "~6.21.0"
      }
    },
    "node_modules/@types/qrcode": {
      "version": "1.5.6",
      "resolved": "https://registry.npmjs.org/@types/qrcode/-/qrcode-1.5.6.tgz",
      "integrity": "sha512-te7NQcV2BOvdj2b1hCAHzAoMNuj65kNBMz0KBaxM6c3VGBOhU0dURQKOtH8CFNI/dsKkwlv32p26qYQTWoB5bw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/node": "*"
      }
    },
    "node_modules/@types/react": {
      "version": "19.3.0",
      "resolved": "https://registry.npmjs.org/@types/react/-/react-19.3.0.tgz",
      "integrity": "sha512-N0rFCuH9YoxG9/m61l9MfpJKfmLOVU0em7ipIz6TRgSSkvReLB9vL85GB+yr8Bs5leqpvg96JSwF4ZS1s4viQg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "csstype": "^3.2.2"
      }
    },
    "node_modules/@types/react-dom": {
      "version": "19.3.0",
      "resolved": "https://registry.npmjs.org/@types/react-dom/-/react-dom-19.3.0.tgz",
      "integrity": "sha512-ZI7bU42mZXXKHn/qNLEw2IrbiINU7X5+vfgdixBHkCNpYWXjKgfQ/P+uyGb5CjOLB9UcnTeg3rylQtV2hym44Q==",
      "dev": true,
      "license": "MIT",
      "peerDependencies": {
        "@types/react": "^19.3.0"
      }
    },
    "node_modules/ansi-regex": {
      "version": "5.0.1",
      "resolved": "https://registry.npmjs.org/ansi-regex/-/ansi-regex-5.0.1.tgz",
      "integrity": "sha512-quJQXlTSUGL2LH9SUXo8VwsY4soanhgo6LNSm84E1LBcE8s3O0wpdiRzyR9z/ZZJMlMWv37qOOb9pdJlMUEKFQ==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/ansi-styles": {
      "version": "4.3.0",
      "resolved": "https://registry.npmjs.org/ansi-styles/-/ansi-styles-4.3.0.tgz",
      "integrity": "sha512-zbB9rCJAT1rbjiVDb2hqKFHNYLxgtk8NURxZ3IZwD3F6NtxbXZQCnnSi1Lkx+IDohdPlFp222wVALIheZJQSEg==",
      "license": "MIT",
      "dependencies": {
        "color-convert": "^2.0.1"
      },
      "engines": {
        "node": ">=8"
      },
      "funding": {
        "url": "https://github.com/chalk/ansi-styles?sponsor=1"
      }
    },
    "node_modules/baseline-browser-mapping": {
      "version": "2.11.35",
      "resolved": "https://registry.npmjs.org/baseline-browser-mapping/-/baseline-browser-mapping-2.11.35.tgz",
      "integrity": "sha512-GNk8KX52CHqeNKGk8+7tZnQab/2k1t/BgrUHPKNdijzpEhF1saPQZHVKb6m5loSAxB39gyrTYw34Qf9CQ3u1qQ==",
      "license": "Apache-2.0",
      "bin": {
        "baseline-browser-mapping": "dist/cli.cjs"
      },
      "engines": {
        "node": ">=6.0.0"
      }
    },
    "node_modules/camelcase": {
      "version": "5.3.1",
      "resolved": "https://registry.npmjs.org/camelcase/-/camelcase-5.3.1.tgz",
      "integrity": "sha512-L28STB170nwWS63UjtlEOE3dldQApaJXZkOI1uMFfzf3rRuPegHaHesyee+YxQ+W6SvRDQV6UrdOdRiR153wJg==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/caniuse-lite": {
      "version": "1.0.30001823",
      "resolved": "https://registry.npmjs.org/caniuse-lite/-/caniuse-lite-1.0.30001823.tgz",
      "integrity": "sha512-TQ5s/djDjNk1axreUW+4rULH+BmdCMLiJkhaXnO5wqivG7tITkSUj4ItIdzqdZHKaXcHAV8dhH3JxOM7/7bwqw==",
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/browserslist"
        },
        {
          "type": "tidelift",
          "url": "https://tidelift.com/funding/github/npm/caniuse-lite"
        },
        {
          "type": "github",
          "url": "https://github.com/sponsors/ai"
        }
      ],
      "license": "CC-BY-4.0"
    },
    "node_modules/client-only": {
      "version": "0.0.1",
      "resolved": "https://registry.npmjs.org/client-only/-/client-only-0.0.1.tgz",
      "integrity": "sha512-IV3Ou0jSMzZrd3pZ48nLkT9DA7Ag1pnPzaiQhpW7c3RbcqqzvzzVu+L8gfqMp/8IM2MQtSiqaCxrrcfu8I8rMA==",
      "license": "MIT"
    },
    "node_modules/cliui": {
      "version": "6.0.0",
      "resolved": "https://registry.npmjs.org/cliui/-/cliui-6.0.0.tgz",
      "integrity": "sha512-t6wbgtoCXvAzst7QgXxJYqPt0usEfbgQdftEPbLL/cvv6HPE5VgvqCuAIDR0NgU52ds6rFwqrgakNLrHEjCbrQ==",
      "license": "ISC",
      "dependencies": {
        "string-width": "^4.2.0",
        "strip-ansi": "^6.0.0",
        "wrap-ansi": "^6.2.0"
      }
    },
    "node_modules/color-convert": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/color-convert/-/color-convert-2.0.1.tgz",
      "integrity": "sha512-RRECPsj7iu/xb5oKYcsFHSppFNnsj/52OVTRKb4zP5onXwVF3zVmmToNcOfGC+CRDpfK/U584fMg38ZHCaElKQ==",
      "license": "MIT",
      "dependencies": {
        "color-name": "~1.1.4"
      },
      "engines": {
        "node": ">=7.0.0"
      }
    },
    "node_modules/color-name": {
      "version": "1.1.4",
      "resolved": "https://registry.npmjs.org/color-name/-/color-name-1.1.4.tgz",
      "integrity": "sha512-dOy+3AuW3a2wNbZHIuMZpTcgjGuLU/uBL/ubcZF9OXbDo8ff4O8yVp5Bf0efS8uEoYo5q4Fx7dY9OgQGXgAsQA==",
      "license": "MIT"
    },
    "node_modules/csstype": {
      "version": "3.2.3",
      "resolved": "https://registry.npmjs.org/csstype/-/csstype-3.2.3.tgz",
      "integrity": "sha512-z1HGKcYy2xA8AGQfwrn0PAy+PB7X/GSj3UVJW9qKyn43xWa+gl5nXmU4qqLMRzWVLFC8KusUX8T/0kCiOYpAIQ==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/decamelize": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/decamelize/-/decamelize-1.2.0.tgz",
      "integrity": "sha512-z2S+W9X73hAUUki+N+9Za2lBlun89zigOyGrsax+KUQ6wKW4ZoWpEYBkGhQjwAjjDCkWxhY0VKEhk8wzY7F5cA==",
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/detect-libc": {
      "version": "2.1.2",
      "resolved": "https://registry.npmjs.org/detect-libc/-/detect-libc-2.1.2.tgz",
      "integrity": "sha512-Btj2BOOO83o3WyH59e8MgXsxEQVcarkUOpEYrubB0urwnN10yQ364rsiByU11nZlqWYZm05i/of7io4mzihBtQ==",
      "devOptional": true,
      "license": "Apache-2.0",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/dijkstrajs": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/dijkstrajs/-/dijkstrajs-1.0.3.tgz",
      "integrity": "sha512-qiSlmBq9+BCdCA/L46dw8Uy93mloxsPSbwnm5yrKn2vMPiy8KyAskTF6zuV/j5BMsmOGZDPs7KjU+mjb670kfA==",
      "license": "MIT"
    },
    "node_modules/emoji-regex": {
      "version": "8.0.0",
      "resolved": "https://registry.npmjs.org/emoji-regex/-/emoji-regex-8.0.0.tgz",
      "integrity": "sha512-MSjYzcWNOA0ewAHpz0MxpYFvwg6yjy1NG3xteoqz644VCo/RPgnr1/GGt+ic3iJTzQ8Eu3TdM14SawnVUmGE6A==",
      "license": "MIT"
    },
    "node_modules/enhanced-resolve": {
      "version": "5.26.1",
      "resolved": "https://registry.npmjs.org/enhanced-resolve/-/enhanced-resolve-5.26.1.tgz",
      "integrity": "sha512-PPnnSJq3azKOIewXR/uppBV/6h98dprBJ/WaQ9Qgj10xX1lJLNfg+XShpbsrSqcDSy2yYYyhfXM1wWhftqgyzw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "graceful-fs": "^4.2.4",
        "tapable": "^2.3.3"
      },
      "engines": {
        "node": ">=10.13.0"
      }
    },
    "node_modules/find-up": {
      "version": "4.1.0",
      "resolved": "https://registry.npmjs.org/find-up/-/find-up-4.1.0.tgz",
      "integrity": "sha512-PpOwAdQ/YlXQ2vj8a3h8IipDuYRi3wceVQQGYWxNINccq40Anw7BlsEXCMbt1Zt+OLA6Fq9suIpIWD0OsnISlw==",
      "license": "MIT",
      "dependencies": {
        "locate-path": "^5.0.0",
        "path-exists": "^4.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/get-caller-file": {
      "version": "2.0.5",
      "resolved": "https://registry.npmjs.org/get-caller-file/-/get-caller-file-2.0.5.tgz",
      "integrity": "sha512-DyFP3BM/3YHTQOCUL/w0OZHR0lpKeGrxotcHWcqNEdnltqFwXVfhEBQ94eIo34AfQpo0rGki4cyIiftY06h2Fg==",
      "license": "ISC",
      "engines": {
        "node": "6.* || 8.* || >= 10.*"
      }
    },
    "node_modules/graceful-fs": {
      "version": "4.2.11",
      "resolved": "https://registry.npmjs.org/graceful-fs/-/graceful-fs-4.2.11.tgz",
      "integrity": "sha512-RbJ5/jmFcNNCcDV5o9eTnBLJ/HszWV0P73bc+Ff4nS/rJj+YaS6IGyiOL0VoBYX+l1Wrl3k63h/KrH+nhJ0XvQ==",
      "dev": true,
      "license": "ISC"
    },
    "node_modules/is-fullwidth-code-point": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/is-fullwidth-code-point/-/is-fullwidth-code-point-3.0.0.tgz",
      "integrity": "sha512-zymm5+u+sCsSWyD9qNaejV3DFvhCKclKdizYaJUuHA83RLjb7nSuGnddCHGv0hk+KY7BMAlsWeK4Ueg6EV6XQg==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/jiti": {
      "version": "2.7.0",
      "resolved": "https://registry.npmjs.org/jiti/-/jiti-2.7.0.tgz",
      "integrity": "sha512-AC/7JofJvZGrrneWNaEnJeOLUx+JlGt7tNa0wZiRPT4MY1wmfKjt2+6O2p2uz2+skll8OZZmJMNqeke7kKbNgQ==",
      "dev": true,
      "license": "MIT",
      "bin": {
        "jiti": "lib/jiti-cli.mjs"
      }
    },
    "node_modules/lightningcss": {
      "version": "1.33.0",
      "resolved": "https://registry.npmjs.org/lightningcss/-/lightningcss-1.33.0.tgz",
      "integrity": "sha512-WkUDrojuJs0xkgGf2udWxa3yGBRxPtxUkB79i6aCZLRgc7PM8fZe9TosfPDcvEpQZbuFASnHYmRLBLUbmLOIIA==",
      "dev": true,
      "license": "MPL-2.0",
      "dependencies": {
        "detect-libc": "^2.0.3"
      },
      "engines": {
        "node": ">= 12.0.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/parcel"
      },
      "optionalDependencies": {
        "lightningcss-android-arm64": "1.33.0",
        "lightningcss-darwin-arm64": "1.33.0",
        "lightningcss-darwin-x64": "1.33.0",
        "lightningcss-freebsd-x64": "1.33.0",
        "lightningcss-linux-arm-gnueabihf": "1.33.0",
        "lightningcss-linux-arm64-gnu": "1.33.0",
        "lightningcss-linux-arm64-musl": "1.33.0",
        "lightningcss-linux-x64-gnu": "1.33.0",
        "lightningcss-linux-x64-musl": "1.33.0",
        "lightningcss-win32-arm64-msvc": "1.33.0",
        "lightningcss-win32-x64-msvc": "1.33.0"
      }
    },
    "node_modules/lightningcss-android-arm64": {
      "version": "1.33.0",
      "resolved": "https://registry.npmjs.org/lightningcss-android-arm64/-/lightningcss-android-arm64-1.33.0.tgz",
      "integrity": "sha512-gEpRTalKdosp4Bb8qWtc2iOgE5SeIHlpS1up9bFq2wAyYhl1UdTObYiHe98zEM9SQvSoqQZ1IQD0JNpg3Ml5pg==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MPL-2.0",
      "optional": true,
      "os": [
        "android"
      ],
      "engines": {
        "node": ">= 12.0.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/parcel"
      }
    },
    "node_modules/lightningcss-darwin-arm64": {
      "version": "1.33.0",
      "resolved": "https://registry.npmjs.org/lightningcss-darwin-arm64/-/lightningcss-darwin-arm64-1.33.0.tgz",
      "integrity": "sha512-Sciaz8eenNTKn9b3t7+xr0ipTp9YxKQY4npwQ3mrRuL0BAVHBLyZxofhaKBAVtzmtRZ/zTyo0/to4B1uWG/Djg==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MPL-2.0",
      "optional": true,
      "os": [
        "darwin"
      ],
      "engines": {
        "node": ">= 12.0.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/parcel"
      }
    },
    "node_modules/lightningcss-darwin-x64": {
      "version": "1.33.0",
      "resolved": "https://registry.npmjs.org/lightningcss-darwin-x64/-/lightningcss-darwin-x64-1.33.0.tgz",
      "integrity": "sha512-Z5UPAxzrjlWNNyGy6i65cJzzvgJ5D3T6wMvs+gWpY9d7qRhANrxqAp6LhxIgZhWEw18RfJTGcRxjuLIBr+m8XQ==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MPL-2.0",
      "optional": true,
      "os": [
        "darwin"
      ],
      "engines": {
        "node": ">= 12.0.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/parcel"
      }
    },
    "node_modules/lightningcss-freebsd-x64": {
      "version": "1.33.0",
      "resolved": "https://registry.npmjs.org/lightningcss-freebsd-x64/-/lightningcss-freebsd-x64-1.33.0.tgz",
      "integrity": "sha512-QQM/Ti/hQajJwCY+RiWuCZ9sdtI/XQk7nDK5vC8kkdwixezOlDgvDx7+RT+QjK6FcFT4MpsuoBnHIo/O3StRRg==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MPL-2.0",
      "optional": true,
      "os": [
        "freebsd"
      ],
      "engines": {
        "node": ">= 12.0.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/parcel"
      }
    },
    "node_modules/lightningcss-linux-arm-gnueabihf": {
      "version": "1.33.0",
      "resolved": "https://registry.npmjs.org/lightningcss-linux-arm-gnueabihf/-/lightningcss-linux-arm-gnueabihf-1.33.0.tgz",
      "integrity": "sha512-N7FVBe6iS24MlM6R/4RBTxGhQheZGs7tiQ9U32UtF75NzP5Q7xWPRqLBCKxlRQRk3rY1jCIPLzx7WzOhuUIRLQ==",
      "cpu": [
        "arm"
      ],
      "dev": true,
      "license": "MPL-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 12.0.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/parcel"
      }
    },
    "node_modules/lightningcss-linux-arm64-gnu": {
      "version": "1.33.0",
      "resolved": "https://registry.npmjs.org/lightningcss-linux-arm64-gnu/-/lightningcss-linux-arm64-gnu-1.33.0.tgz",
      "integrity": "sha512-j2v/itmy4HlNxlc6voKXYgBqNi0Ng2LShg4z7GufpEgs05P+2suBVyi9I6YHq5uoVFx9ETin3eCEhLVyXGQnKg==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "libc": [
        "glibc"
      ],
      "license": "MPL-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 12.0.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/parcel"
      }
    },
    "node_modules/lightningcss-linux-arm64-musl": {
      "version": "1.33.0",
      "resolved": "https://registry.npmjs.org/lightningcss-linux-arm64-musl/-/lightningcss-linux-arm64-musl-1.33.0.tgz",
      "integrity": "sha512-yiO5ROMuYQgXbC60yjZU5CYSFZGKXL0HFATXt9mHJn1+zW55oCtMI9NfcVhYLMFDL7gV7oBPon/EmMMGg2OvtQ==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "libc": [
        "musl"
      ],
      "license": "MPL-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 12.0.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/parcel"
      }
    },
    "node_modules/lightningcss-linux-x64-gnu": {
      "version": "1.33.0",
      "resolved": "https://registry.npmjs.org/lightningcss-linux-x64-gnu/-/lightningcss-linux-x64-gnu-1.33.0.tgz",
      "integrity": "sha512-ar+Ju7LmcN0Jo4FpL4hpFybwNG9/3A/Br5KW2n2jyODg3MEZXaDYADdemoNS+BDNfMgKvylJLj4S5tyRActuAg==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "libc": [
        "glibc"
      ],
      "license": "MPL-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 12.0.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/parcel"
      }
    },
    "node_modules/lightningcss-linux-x64-musl": {
      "version": "1.33.0",
      "resolved": "https://registry.npmjs.org/lightningcss-linux-x64-musl/-/lightningcss-linux-x64-musl-1.33.0.tgz",
      "integrity": "sha512-RYiYbkokw0trfKqqzfF55lginwEPrD3OJDfTuJzFs1MK6iFnDenaz1fqLLtX4ITG3OktJQXOeTaw1awrBAlZPw==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "libc": [
        "musl"
      ],
      "license": "MPL-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">= 12.0.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/parcel"
      }
    },
    "node_modules/lightningcss-win32-arm64-msvc": {
      "version": "1.33.0",
      "resolved": "https://registry.npmjs.org/lightningcss-win32-arm64-msvc/-/lightningcss-win32-arm64-msvc-1.33.0.tgz",
      "integrity": "sha512-1K+MPfLSFVpphzpdbfkhlWk6wBrTObBzS2T6db10PNOZgR9GoVsAWzwNyuhUYYbTp23j+4RrncfujZ4uAzXvwA==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MPL-2.0",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">= 12.0.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/parcel"
      }
    },
    "node_modules/lightningcss-win32-x64-msvc": {
      "version": "1.33.0",
      "resolved": "https://registry.npmjs.org/lightningcss-win32-x64-msvc/-/lightningcss-win32-x64-msvc-1.33.0.tgz",
      "integrity": "sha512-OlEICDx/Xl0FqSp4bry8zFnCvGpig3Gl4gCquvYwHuqJKEC1+n9NgDniFvqHGmMv1ZkqDJrDqKKSykTDX+ehuA==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MPL-2.0",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">= 12.0.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/parcel"
      }
    },
    "node_modules/locate-path": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/locate-path/-/locate-path-5.0.0.tgz",
      "integrity": "sha512-t7hw9pI+WvuwNJXwk5zVHpyhIqzg2qTlklJOf0mVxGSbe3Fp2VieZcduNYjaLDoy6p9uGpQEGWG87WpMKlNq8g==",
      "license": "MIT",
      "dependencies": {
        "p-locate": "^4.1.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/magic-string": {
      "version": "1.4.5",
      "resolved": "https://registry.npmjs.org/magic-string/-/magic-string-1.4.5.tgz",
      "integrity": "sha512-oLLC2+YvQUfAa+vxoufE/yc1icb87M9iXIRqAoR/2EhE/8cb3SF/+Gi0c2By1B+5Vz2e2vQtUvHiu1+63Znh+w==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@jridgewell/sourcemap-codec": "^1.6.0"
      }
    },
    "node_modules/nanoid": {
      "version": "3.3.20",
      "resolved": "https://registry.npmjs.org/nanoid/-/nanoid-3.3.20.tgz",
      "integrity": "sha512-uKdg2G3GNCKQn9byYOpxbGqrT2fGO5KRt5J/8b3pok8rT6qxGWF6hxMyJiEYtAf+FVyYuD9hRaDqX5uPFYJ4ZQ==",
      "funding": [
        {
          "type": "github",
          "url": "https://github.com/sponsors/ai"
        }
      ],
      "license": "MIT",
      "bin": {
        "nanoid": "bin/nanoid.cjs"
      },
      "engines": {
        "node": "^10 || ^12 || ^13.7 || ^14 || >=15.0.1"
      }
    },
    "node_modules/next": {
      "version": "16.4.6",
      "resolved": "https://registry.npmjs.org/next/-/next-16.4.6.tgz",
      "integrity": "sha512-QZJiYhaZLJMo2KpkQGQIwvmd79WVsAWeYIU554a8d7zArS3si/IRy3lBNV/rtYhE70oLwdLYhPAXLPx8HwcwtA==",
      "license": "MIT",
      "dependencies": {
        "@next/env": "16.4.6",
        "@swc/helpers": "0.5.23",
        "baseline-browser-mapping": "^2.9.19",
        "caniuse-lite": "^1.0.30001579",
        "postcss": "8.5.23",
        "styled-jsx": "5.1.6"
      },
      "bin": {
        "next": "dist/bin/next"
      },
      "engines": {
        "node": ">=20.9.0"
      },
      "optionalDependencies": {
        "@next/swc-darwin-arm64": "16.4.6",
        "@next/swc-darwin-x64": "16.4.6",
        "@next/swc-linux-arm64-gnu": "16.4.6",
        "@next/swc-linux-arm64-musl": "16.4.6",
        "@next/swc-linux-x64-gnu": "16.4.6",
        "@next/swc-linux-x64-musl": "16.4.6",
        "@next/swc-win32-arm64-msvc": "16.4.6",
        "@next/swc-win32-x64-msvc": "16.4.6",
        "sharp": "^0.35.5"
      },
      "peerDependencies": {
        "@opentelemetry/api": "^1.1.0",
        "@playwright/test": "^1.51.1",
        "babel-plugin-react-compiler": "*",
        "react": "^18.2.0 || 19.0.0-rc-de68d2f4-20241204 || ^19.0.0",
        "react-dom": "^18.2.0 || 19.0.0-rc-de68d2f4-20241204 || ^19.0.0",
        "sass": "^1.3.0"
      },
      "peerDependenciesMeta": {
        "@opentelemetry/api": {
          "optional": true
        },
        "@playwright/test": {
          "optional": true
        },
        "babel-plugin-react-compiler": {
          "optional": true
        },
        "sass": {
          "optional": true
        }
      }
    },
    "node_modules/next/node_modules/postcss": {
      "version": "8.5.23",
      "resolved": "https://registry.npmjs.org/postcss/-/postcss-8.5.23.tgz",
      "integrity": "sha512-g50586zr4bZmwFiTlflMu8E0bDTb5I5gertgwAKmsdUlTQIhZtunzUlD1WSzwcVWPoAVpsrA6vlfCD7oXvRwgg==",
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/postcss/"
        },
        {
          "type": "tidelift",
          "url": "https://tidelift.com/funding/github/npm/postcss"
        },
        {
          "type": "github",
          "url": "https://github.com/sponsors/ai"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "nanoid": "^3.3.16",
        "picocolors": "^1.1.1",
        "source-map-js": "^1.2.1"
      },
      "engines": {
        "node": "^10 || ^12 || >=14"
      }
    },
    "node_modules/p-limit": {
      "version": "2.3.0",
      "resolved": "https://registry.npmjs.org/p-limit/-/p-limit-2.3.0.tgz",
      "integrity": "sha512-//88mFWSJx8lxCzwdAABTJL2MyWB12+eIY7MDL2SqLmAkeKU9qxRvWuSyTjm3FUmpBEMuFfckAIqEaVGUDxb6w==",
      "license": "MIT",
      "dependencies": {
        "p-try": "^2.0.0"
      },
      "engines": {
        "node": ">=6"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/p-locate": {
      "version": "4.1.0",
      "resolved": "https://registry.npmjs.org/p-locate/-/p-locate-4.1.0.tgz",
      "integrity": "sha512-R79ZZ/0wAxKGu3oYMlz8jy/kbhsNrS7SKZ7PxEHBgJ5+F2mtFW2fK2cOtBh1cHYkQsbzFV7I+EoRKe6Yt0oK7A==",
      "license": "MIT",
      "dependencies": {
        "p-limit": "^2.2.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/p-try": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/p-try/-/p-try-2.2.0.tgz",
      "integrity": "sha512-R4nPAVTAU0B9D35/Gk3uJf/7XYbQcyohSKdvAxIRSNghFl4e71hVoGnBNQz9cWaXxO2I10KTC+3jMdvvoKw6dQ==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/path-exists": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/path-exists/-/path-exists-4.0.0.tgz",
      "integrity": "sha512-ak9Qy5Q7jYb2Wwcey5Fpvg2KoAc/ZIhLSLOSBmRmygPsGwkVVt0fZa0qrtMz+m6tJTAHfZQ8FnmB4MG4LWy7/w==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/picocolors": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/picocolors/-/picocolors-1.1.1.tgz",
      "integrity": "sha512-xceH2snhtb5M9liqDsmEw56le376mTZkEX/jEb/RxNFyegNul7eNslCXP9FDj/Lcu0X8KEyMceP2ntpaHrDEVA==",
      "license": "ISC"
    },
    "node_modules/pngjs": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/pngjs/-/pngjs-5.0.0.tgz",
      "integrity": "sha512-40QW5YalBNfQo5yRYmiw7Yz6TKKVr3h6970B2YE+3fQpsWcrbj1PzJgxeJ19DRQjhMbKPIuMY8rFaXc8moolVw==",
      "license": "MIT",
      "engines": {
        "node": ">=10.13.0"
      }
    },
    "node_modules/postcss": {
      "version": "8.5.32",
      "resolved": "https://registry.npmjs.org/postcss/-/postcss-8.5.32.tgz",
      "integrity": "sha512-LJlKCCAUFKOuZxipUdYw1NzIITEsPcgyOG9LkvRJvuKj/bRzbuRY0ARXvL0pWGpsZvn8jku+LMep2eU0seHp8g==",
      "dev": true,
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/postcss/"
        },
        {
          "type": "tidelift",
          "url": "https://tidelift.com/funding/github/npm/postcss"
        },
        {
          "type": "github",
          "url": "https://github.com/sponsors/ai"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "nanoid": "^3.3.20",
        "picocolors": "^1.1.1",
        "source-map-js": "^1.2.2"
      },
      "engines": {
        "node": "^10 || ^12 || >=14"
      }
    },
    "node_modules/qrcode": {
      "version": "1.5.4",
      "resolved": "https://registry.npmjs.org/qrcode/-/qrcode-1.5.4.tgz",
      "integrity": "sha512-1ca71Zgiu6ORjHqFBDpnSMTR2ReToX4l1Au1VFLyVeBTFavzQnv5JxMFr3ukHVKpSrSA2MCk0lNJSykjUfz7Zg==",
      "license": "MIT",
      "dependencies": {
        "dijkstrajs": "^1.0.1",
        "pngjs": "^5.0.0",
        "yargs": "^15.3.1"
      },
      "bin": {
        "qrcode": "bin/qrcode"
      },
      "engines": {
        "node": ">=10.13.0"
      }
    },
    "node_modules/react": {
      "version": "19.3.1",
      "resolved": "https://registry.npmjs.org/react/-/react-19.3.1.tgz",
      "integrity": "sha512-QNhWdt7nrgVWWQG58QuGsAR3jv3Hbe4mb4vz7w2csnHavciZJgda1CPNaldF6eVxv90ud3jUXpKlHL69gO38yw==",
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/react-dom": {
      "version": "19.3.1",
      "resolved": "https://registry.npmjs.org/react-dom/-/react-dom-19.3.1.tgz",
      "integrity": "sha512-Y0bARz53lhEC1NMCASs0/j+faB/zqt3R8hpvg1e8+61ZVJ4UL0UdC4cBbXfZMcIuhrfgeILTLe+ZeBCavQPtKQ==",
      "license": "MIT",
      "dependencies": {
        "scheduler": "^0.28.0"
      },
      "peerDependencies": {
        "react": "^19.3.1"
      }
    },
    "node_modules/require-directory": {
      "version": "2.1.1",
      "resolved": "https://registry.npmjs.org/require-directory/-/require-directory-2.1.1.tgz",
      "integrity": "sha512-fGxEI7+wsG9xrvdjsrlmL22OMTTiHRwAMroiEeMgq8gzoLC/PQr7RsRDSTLUg/bZAZtF+TVIkHc6/4RIKrui+Q==",
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/require-main-filename": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/require-main-filename/-/require-main-filename-2.0.0.tgz",
      "integrity": "sha512-NKN5kMDylKuldxYLSUfrbo5Tuzh4hd+2E8NPPX02mZtn1VuREQToYe/ZdlJy+J3uCpfaiGF05e7B8W0iXbQHmg==",
      "license": "ISC"
    },
    "node_modules/scheduler": {
      "version": "0.28.0",
      "resolved": "https://registry.npmjs.org/scheduler/-/scheduler-0.28.0.tgz",
      "integrity": "sha512-juorfCmIkIw8tT+p5BXSm6PJjQF/ycEYmKyzURCIt/RaZIhL+PulbQ9Yu2z1HdOJDdqDTlxA1+xKBmHXJsczAw==",
      "license": "MIT"
    },
    "node_modules/semver": {
      "version": "7.8.6",
      "resolved": "https://registry.npmjs.org/semver/-/semver-7.8.6.tgz",
      "integrity": "sha512-9lpSSU4Mly3mrtruwLs1eLK6+gzbzqeBFwRNjIjE+9LuDpWdYctrQlQ3ej1Ilgi7gknpsTRnPoLP8DpCHqHIJw==",
      "license": "ISC",
      "optional": true,
      "bin": {
        "semver": "bin/semver.js"
      },
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/set-blocking": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/set-blocking/-/set-blocking-2.0.0.tgz",
      "integrity": "sha512-KiKBS8AnWGEyLzofFfmvKwpdPzqiy16LvQfK3yv/fVH7Bj13/wl3JSR1J+rfgRE9q7xUJK4qvgS8raSOeLUehw==",
      "license": "ISC"
    },
    "node_modules/sharp": {
      "version": "0.35.5",
      "resolved": "https://registry.npmjs.org/sharp/-/sharp-0.35.5.tgz",
      "integrity": "sha512-Ywn4OnzGukp7CDMrp08RQ50YKmuwG47brZgIVPTvBaaAfQlRlygrRqSrxdCiL9M+LlzLBiJ68IR1QqvzHyjC7g==",
      "license": "Apache-2.0",
      "optional": true,
      "dependencies": {
        "@img/colour": "^1.1.0",
        "detect-libc": "^2.1.2",
        "semver": "^7.8.5"
      },
      "engines": {
        "node": ">=20.9.0"
      },
      "funding": {
        "url": "https://opencollective.com/libvips"
      },
      "optionalDependencies": {
        "@img/sharp-darwin-arm64": "0.35.5",
        "@img/sharp-darwin-x64": "0.35.5",
        "@img/sharp-freebsd-wasm32": "0.35.5",
        "@img/sharp-libvips-darwin-arm64": "1.3.4",
        "@img/sharp-libvips-darwin-x64": "1.3.4",
        "@img/sharp-libvips-linux-arm": "1.3.4",
        "@img/sharp-libvips-linux-arm64": "1.3.4",
        "@img/sharp-libvips-linux-ppc64": "1.3.4",
        "@img/sharp-libvips-linux-riscv64": "1.3.4",
        "@img/sharp-libvips-linux-s390x": "1.3.4",
        "@img/sharp-libvips-linux-x64": "1.3.4",
        "@img/sharp-libvips-linuxmusl-arm64": "1.3.4",
        "@img/sharp-libvips-linuxmusl-x64": "1.3.4",
        "@img/sharp-linux-arm": "0.35.5",
        "@img/sharp-linux-arm64": "0.35.5",
        "@img/sharp-linux-ppc64": "0.35.5",
        "@img/sharp-linux-riscv64": "0.35.5",
        "@img/sharp-linux-s390x": "0.35.5",
        "@img/sharp-linux-x64": "0.35.5",
        "@img/sharp-linuxmusl-arm64": "0.35.5",
        "@img/sharp-linuxmusl-x64": "0.35.5",
        "@img/sharp-webcontainers-wasm32": "0.35.5",
        "@img/sharp-win32-arm64": "0.35.5",
        "@img/sharp-win32-ia32": "0.35.5",
        "@img/sharp-win32-x64": "0.35.5"
      },
      "peerDependenciesMeta": {
        "@types/node": {
          "optional": true
        }
      }
    },
    "node_modules/source-map-js": {
      "version": "1.2.2",
      "resolved": "https://registry.npmjs.org/source-map-js/-/source-map-js-1.2.2.tgz",
      "integrity": "sha512-KGj/8Y43x35aZVDtt+J4mK1hoLGHULMYfSkODJNQjNDC3oW1PqPoxMwo0pLUsWM/UEGzON/NxeHywEfNXNP3Vw==",
      "license": "BSD-3-Clause",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/string-width": {
      "version": "4.2.3",
      "resolved": "https://registry.npmjs.org/string-width/-/string-width-4.2.3.tgz",
      "integrity": "sha512-wKyQRQpjJ0sIp62ErSZdGsjMJWsap5oRNihHhu6G7JVO/9jIB6UyevL+tXuOqrng8j/cxKTWyWUwvSTriiZz/g==",
      "license": "MIT",
      "dependencies": {
        "emoji-regex": "^8.0.0",
        "is-fullwidth-code-point": "^3.0.0",
        "strip-ansi": "^6.0.1"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/strip-ansi": {
      "version": "6.0.1",
      "resolved": "https://registry.npmjs.org/strip-ansi/-/strip-ansi-6.0.1.tgz",
      "integrity": "sha512-Y38VPSHcqkFrCpFnQ9vuSXmquuv5oXOKpGeT6aGrr3o3Gc9AlVa6JBfUSOCnbxGGZF+/0ooI7KrPuUSztUdU5A==",
      "license": "MIT",
      "dependencies": {
        "ansi-regex": "^5.0.1"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/styled-jsx": {
      "version": "5.1.6",
      "resolved": "https://registry.npmjs.org/styled-jsx/-/styled-jsx-5.1.6.tgz",
      "integrity": "sha512-qSVyDTeMotdvQYoHWLNGwRFJHC+i+ZvdBRYosOFgC+Wg1vx4frN2/RG/NA7SYqqvKNLf39P2LSRA2pu6n0XYZA==",
      "license": "MIT",
      "dependencies": {
        "client-only": "0.0.1"
      },
      "engines": {
        "node": ">= 12.0.0"
      },
      "peerDependencies": {
        "react": ">= 16.8.0 || 17.x.x || ^18.0.0-0 || ^19.0.0-0"
      },
      "peerDependenciesMeta": {
        "@babel/core": {
          "optional": true
        },
        "babel-plugin-macros": {
          "optional": true
        }
      }
    },
    "node_modules/tailwindcss": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/tailwindcss/-/tailwindcss-4.3.5.tgz",
      "integrity": "sha512-FcQk9BuffmEHJP2G0XmB2SplU1aLTI7j07Kunk+U74Ny+XiWOtzXz9aujFZ/avntw1e2cOv/3PkgzflQ7gX2vQ==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/tapable": {
      "version": "2.3.3",
      "resolved": "https://registry.npmjs.org/tapable/-/tapable-2.3.3.tgz",
      "integrity": "sha512-uxc/zpqFg6x7C8vOE7lh6Lbda8eEL9zmVm/PLeTPBRhh1xCgdWaQ+J1CUieGpIfm2HdtsUpRv+HshiasBMcc6A==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=6"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/webpack"
      }
    },
    "node_modules/tslib": {
      "version": "2.9.1",
      "resolved": "https://registry.npmjs.org/tslib/-/tslib-2.9.1.tgz",
      "integrity": "sha512-a4Ux9VKuIMHsOS7ENbEq6hK2ZGYIT27Rtl0E4eD9KqwxhKiQeMZE/9xb3IdYwWaSOyIBQLExhQgXDTYoiCxnWA==",
      "license": "0BSD"
    },
    "node_modules/typescript": {
      "version": "5.9.3",
      "resolved": "https://registry.npmjs.org/typescript/-/typescript-5.9.3.tgz",
      "integrity": "sha512-jl1vZzPDinLr9eUt3J/t7V6FgNEw9QjvBPdysz9KfQDD41fQrC2Y4vKQdiaUpFT4bXlb1RHhLpp8wtm6M5TgSw==",
      "dev": true,
      "license": "Apache-2.0",
      "bin": {
        "tsc": "bin/tsc",
        "tsserver": "bin/tsserver"
      },
      "engines": {
        "node": ">=14.17"
      }
    },
    "node_modules/undici-types": {
      "version": "6.21.0",
      "resolved": "https://registry.npmjs.org/undici-types/-/undici-types-6.21.0.tgz",
      "integrity": "sha512-iwDZqg0QAGrg9Rav5H4n0M64c3mkR59cJ6wQp+7C4nI0gsmExaedaYLNO44eT4AtBBwjbTiGPMlt2Md0T9H9JQ==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/which-module": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/which-module/-/which-module-2.0.1.tgz",
      "integrity": "sha512-iBdZ57RDvnOR9AGBhML2vFZf7h8vmBjhoaZqODJBFWHVtKkDmKuHai3cx5PgVMrX5YDNp27AofYbAwctSS+vhQ==",
      "license": "ISC"
    },
    "node_modules/wrap-ansi": {
      "version": "6.2.0",
      "resolved": "https://registry.npmjs.org/wrap-ansi/-/wrap-ansi-6.2.0.tgz",
      "integrity": "sha512-r6lPcBGxZXlIcymEu7InxDMhdW0KDxpLgoFLcguasxCaJ/SOIZwINatK9KY/tf+ZrlywOKU0UDj3ATXUBfxJXA==",
      "license": "MIT",
      "dependencies": {
        "ansi-styles": "^4.0.0",
        "string-width": "^4.1.0",
        "strip-ansi": "^6.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/y18n": {
      "version": "4.0.3",
      "resolved": "https://registry.npmjs.org/y18n/-/y18n-4.0.3.tgz",
      "integrity": "sha512-JKhqTOwSrqNA1NY5lSztJ1GrBiUodLMmIZuLiDaMRJ+itFd+ABVE8XBjOvIWL+rSqNDC74LCSFmlb/U4UZ4hJQ==",
      "license": "ISC"
    },
    "node_modules/yargs": {
      "version": "15.4.1",
      "resolved": "https://registry.npmjs.org/yargs/-/yargs-15.4.1.tgz",
      "integrity": "sha512-aePbxDmcYW++PaqBsJ+HYUFwCdv4LVvdnhBy78E57PIor8/OVvhMrADFFEDh8DHDFRv/O9i3lPhsENjO7QX0+A==",
      "license": "MIT",
      "dependencies": {
        "cliui": "^6.0.0",
        "decamelize": "^1.2.0",
        "find-up": "^4.1.0",
        "get-caller-file": "^2.0.1",
        "require-directory": "^2.1.1",
        "require-main-filename": "^2.0.0",
        "set-blocking": "^2.0.0",
        "string-width": "^4.2.0",
        "which-module": "^2.0.0",
        "y18n": "^4.0.0",
        "yargs-parser": "^18.1.2"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/yargs-parser": {
      "version": "18.1.3",
      "resolved": "https://registry.npmjs.org/yargs-parser/-/yargs-parser-18.1.3.tgz",
      "integrity": "sha512-o50j0JeToy/4K6OZcaQmW6lyXXKhq7csREXcDwk2omFPJEwUNOVtJKvmDr9EI1fAJZUyZcRF7kxGBWmRXudrCQ==",
      "license": "ISC",
      "dependencies": {
        "camelcase": "^5.0.0",
        "decamelize": "^1.2.0"
      },
      "engines": {
        "node": ">=6"
      }
    }
  }
}
```

## Fichier package.json

```json
{
  "name": "atelier-prenom",
  "version": "0.1.0",
  "private": true,
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start --hostname 0.0.0.0",
    "typecheck": "tsc --noEmit",
    "handoff": "node scripts/export-handoff.mjs"
  },
  "dependencies": {
    "next": "16.4.6",
    "qrcode": "^1.5.4",
    "react": "19",
    "react-dom": "19"
  },
  "devDependencies": {
    "@tailwindcss/postcss": "4.3.5",
    "@types/node": "^22",
    "@types/qrcode": "^1.5.6",
    "@types/react": "^19",
    "@types/react-dom": "^19",
    "tailwindcss": "4.3.5",
    "typescript": "^5"
  },
  "engines": {
    "node": "22.x"
  }
}
```

## Fichier postcss.config.mjs

```javascript
export default { plugins: { '@tailwindcss/postcss': {} } };
```

## Fichier production/README.md

````markdown
# Prototypes originaux MustDesign3D — privés

Version 2, 10 novembre 2026. Ces sept sources paramétriques ont été écrites pour MustDesign3D. Le manifeste associe chaque fichier à l’identifiant stable du produit. Les sources et exports sont privés. Les vues PNG générées par OpenSCAD sont dans public/models/.

## Statut réel

**À valider pour fabrication.** Les sept assemblages par défaut ont été compilés et exportés en STL avec OpenSCAD 2021.01 portable. Leurs dimensions mesurées respectent l’enveloppe de 220 mm. Les exports de contrôle sont dans exports/. Les vues PNG sont des aperçus OpenSCAD des sources correspondantes. L’aperçu interactif des personnalisations reste une composition 2D indépendante. Slicing, temps de production, tolérances et impressions physiques restent à vérifier.

| Source | Produit | Enveloppe conceptuelle | Couleurs | Parties à exporter |
| --- | --- | --- | --- | --- |
| [porte-cles-prenom.scad](./porte-cles-prenom.scad) | md-keychain-01 | 75 × 28 × 3,6 mm | 2 | base, lettering |
| [plaque-bureau.scad](./plaque-bureau.scad) | md-desk-01 | 160 × 45 × 55 mm assemblé | 3 | foot, panel-base, panel-lettering |
| [ville-maroc.scad](./ville-maroc.scad) | md-city-01 | 180 × 35 × 95 mm assemblé | 3 | foot, silhouette, lettering |
| [support-qr.scad](./support-qr.scad) | md-qr-01 | 90 × 55 × 125 mm assemblé | 3 | foot, panel-base, placeholder |
| [logo-bureau.scad](./logo-bureau.scad) | md-logo-01 | 160 × 40 × 93 mm environ | 2 | foot, monogram |
| [plaque-porte.scad](./plaque-porte.scad) | md-door-01 | 150 × 65 × 4 mm | 3 | base, border, lettering |
| [plaque-pixel-zellige.scad](./plaque-pixel-zellige.scad) | md-pixel-01 | 86 × 86 × 3,6 mm | 3 | base, petals, center |

`assembly` est la valeur initiale de `part`. Les assertions limitent les dimensions principales ; elles ne remplacent pas une revue de géométrie pour chaque changement. Le QR est un cadre et losange **non scannables**, explicitement nommés `non_scannable_qr_placeholder`. La ville est une silhouette abstraite `skyline_placeholder_outline`, sans prétention de fidélité à un monument. Le logo est notre gabarit `original_monogram_placeholder_outline`, pas un logo client.

## Première ouverture et export

1. Installer OpenSCAD localement. Ouvrir une source, régler les paramètres, afficher l’assemblage puis effectuer le rendu complet (F6). Contrôler les avertissements et les volumes non manifold.
2. Tester chaque partie avec `part`. Exporter chaque couleur séparément ; les exports texte restent au même emplacement relatif que la base. Exemple indicatif, à exécuter après installation :

```powershell
openscad -o keychain-base.stl -D 'part="base"' porte-cles-prenom.scad
openscad -o keychain-text.stl -D 'part="lettering"' porte-cles-prenom.scad
```

3. Dans Bambu Studio, charger les parties d’une même plaque comme un objet multiparties, conserver leur repérage puis affecter les filaments AMS Lite. Les couleurs OpenSCAD ne sont pas conservées dans un STL. Enregistrer un 3MF de travail après réglage.
4. Les panneaux se préparent **à plat**, séparément des pieds. Le paramètre `assembly` sert à inspecter l’objet monté et ne définit pas l’orientation de slicing. Pour ville/logo, prévoir une liaison collée entre pied et silhouette ; aucune tenue sans collage n’est garantie. Les pieds bureau/QR utilisent une rainure expérimentale, jeu 0,4 mm à tester. Ne pas imprimer aveuglément l’assemblage dressé.
5. Partir du profil A1, buse 0,4 mm, PLA, couche 0,20 mm, deux à trois couleurs parmi les quatre maximum de l’AMS Lite. Ce sont des paramètres d’essai, pas une recette validée. Vérifier les limites 220 mm souhaitées et la place du brim/purge sur le plateau.
6. Inspecter les premières couches, épaisseurs de lettres, îlots, accroches, transitions de couleur, purge et supports éventuels. Mesurer matière utile, purge, temps, composants, emballage et travail avant de chiffrer.
7. Imprimer un prototype et vérifier lisibilité, solidité, perçages, assemblage, stabilité et tenue des fixations. Pour le QR définitif, générer un véritable code depuis l’URL approuvée, avec zone calme et contraste suffisants, puis tester plusieurs téléphones et angles sur l’objet imprimé.

## Texte, polices et arabe

La police par défaut est `Liberation Sans:style=Bold`, **non fournie**. Vérifier sa présence et ses droits sur le poste ; toute police substituée doit être revue séparément. Aucun fichier de police n’est inclus ou redistribué.

L’aperçu navigateur sait composer les graphèmes et joindre l’arabe. OpenSCAD, les polices locales et le moteur de rendu ne garantissent pas le même résultat. `len()` et l’échelle de texte des prototypes sont des approximations géométriques, pas la validation de graphèmes du site. La saisie web n’est pas reliée automatiquement au CAD. Ne pas inverser les lettres arabes manuellement : faire vérifier le texte et ses diacritiques par une personne compétente, puis importer si nécessaire un tracé SVG correctement façonné et dont les droits sont validés. Ajuster la taille, les deux lignes et l’épaisseur sur chaque prénom long ou bilingue.

Les tolérances, traitements de surface, fixation murale, résistance à la chaleur, usage extérieur et sécurité ne sont pas qualifiés. Pas d’usage alimentaire ni de promesse de tenue. Publier un produit `active` seulement après revue des droits, prototype approuvé, photos originales et prix commercial confirmé.

## Provenance et propriété

[manifest.json](./manifest.json) décrit l’auteur de génération, la date, les liens produit et les empreintes des sept sources, ainsi que leurs dimensions exportées. Les permissions de commercialisation/modification/redistribution restent `null` en attente de décision du propriétaire. Les fichiers numériques sont privés. Les 227 liens du relevé concurrent restent dans la recherche.
````

## Fichier production/logo-bureau.scad

```scad
part = "assembly";
width = 150;
height = 85;
foot_depth = 40;
foot_height = 8;
emblem_thickness = 5;
$fn = 48;

assert(width <= 220 && height+foot_height <= 220 && foot_depth <= 100);

module original_monogram_placeholder_outline() {
  difference() {
    polygon([[-width/2,0],[-width/2,height*0.7],[-width*0.24,height*0.55],[0,height],[width*0.24,height*0.55],[width/2,height*0.7],[width/2,0]]);
    translate([0,height*0.43]) rotate(45) square([height*0.27,height*0.27],center=true);
  }
}

module monogram() {
  color("#efdfc1") linear_extrude(emblem_thickness) original_monogram_placeholder_outline();
}

module foot() {
  color("#233d99") linear_extrude(foot_height) offset(r=3) square([width+4,foot_depth-6],center=true);
}

if (part == "foot" || part == "assembly") foot();
if (part == "monogram") monogram();
if (part == "assembly") translate([0,emblem_thickness/2,foot_height]) rotate([90,0,0]) monogram();
```

## Fichier production/manifest.json

```json
{
  "schemaVersion": 1,
  "createdAt": "2026-11-10",
  "scope": "Private original parametric concept sources; demo only; unvalidated for manufacture",
  "author": "Codex Builder, generated for MustDesign3D at the owner's request",
  "ownershipEvidenceRef": "README.md",
  "externalAssetsAcquired": [],
  "webMedia": {
    "source": "../app/product-art.tsx",
    "provenance": "Six original SVG/HTML compositions created for this iteration; independent of CAD sources; not photographs or manufacturing previews",
    "thirdPartyModelsOrImages": false,
    "fontFilesRedistributed": false,
    "cadRenders": {
      "directory": "../public/models",
      "source": "OpenSCAD 2021.01 preview of the seven original SCAD files",
      "manufactureValidated": false
    }
  },
  "models": [
    {
      "id": "prototype-md-logo-01",
      "productId": "md-logo-01",
      "version": 1,
      "format": "scad",
      "privateStorageKey": "production/logo-bureau.scad",
      "sha256": "cebef7b14bd4699fc1ea59b85b02889e26e98420b64cf8ec9e9c75195cb447e5",
      "sourceType": "original",
      "sourceUrl": null,
      "creator": "Codex Builder for MustDesign3D",
      "licenceLabel": "Owner review pending; not a public downloadable asset",
      "permissions": {
        "commercialPrint": null,
        "modify": null,
        "redistribute": null
      },
      "reviewStatus": "needs_review",
      "rightsEvidenceRef": "README.md",
      "prototypeStatus": "unvalidated",
      "compiled": true,
      "slicedAt": null,
      "manufacturing": {
        "material": "PLA concept",
        "colorCount": 2,
        "filamentGrams": null,
        "purgeGrams": null,
        "printHours": null,
        "productionCostCents": null,
        "supportRequired": null
      },
      "geometryCheck": {
        "tool": "OpenSCAD 2021.01",
        "exportedAt": "2026-11-10",
        "stlVertices": 756,
        "dimensionsMm": [
          160,
          40,
          93
        ],
        "exportRef": "exports/logo-bureau.stl",
        "imageRef": "../public/models/logo-bureau.png"
      }
    },
    {
      "id": "prototype-md-desk-01",
      "productId": "md-desk-01",
      "version": 1,
      "format": "scad",
      "privateStorageKey": "production/plaque-bureau.scad",
      "sha256": "5db040b85f8a178d965aa3acee6b738dde66c1bcb800ad309015b26988d29710",
      "sourceType": "original",
      "sourceUrl": null,
      "creator": "Codex Builder for MustDesign3D",
      "licenceLabel": "Owner review pending; not a public downloadable asset",
      "permissions": {
        "commercialPrint": null,
        "modify": null,
        "redistribute": null
      },
      "reviewStatus": "needs_review",
      "rightsEvidenceRef": "README.md",
      "prototypeStatus": "unvalidated",
      "compiled": true,
      "slicedAt": null,
      "manufacturing": {
        "material": "PLA concept",
        "colorCount": 3,
        "filamentGrams": null,
        "purgeGrams": null,
        "printHours": null,
        "productionCostCents": null,
        "supportRequired": null
      },
      "geometryCheck": {
        "tool": "OpenSCAD 2021.01",
        "exportedAt": "2026-11-10",
        "stlVertices": 10212,
        "dimensionsMm": [
          160,
          45,
          55
        ],
        "exportRef": "exports/plaque-bureau.stl",
        "imageRef": "../public/models/plaque-bureau.png"
      }
    },
    {
      "id": "prototype-md-door-01",
      "productId": "md-door-01",
      "version": 1,
      "format": "scad",
      "privateStorageKey": "production/plaque-porte.scad",
      "sha256": "2685e6fb37f6d3e1d022cd9ae4b19aed503a026b5d1732ad6ae8d96bb05d4e65",
      "sourceType": "original",
      "sourceUrl": null,
      "creator": "Codex Builder for MustDesign3D",
      "licenceLabel": "Owner review pending; not a public downloadable asset",
      "permissions": {
        "commercialPrint": null,
        "modify": null,
        "redistribute": null
      },
      "reviewStatus": "needs_review",
      "rightsEvidenceRef": "README.md",
      "prototypeStatus": "unvalidated",
      "compiled": true,
      "slicedAt": null,
      "manufacturing": {
        "material": "PLA concept",
        "colorCount": 3,
        "filamentGrams": null,
        "purgeGrams": null,
        "printHours": null,
        "productionCostCents": null,
        "supportRequired": null
      },
      "geometryCheck": {
        "tool": "OpenSCAD 2021.01",
        "exportedAt": "2026-11-10",
        "stlVertices": 12684,
        "dimensionsMm": [
          150,
          65,
          4
        ],
        "exportRef": "exports/plaque-porte.stl",
        "imageRef": "../public/models/plaque-porte.png"
      }
    },
    {
      "id": "prototype-md-keychain-01",
      "productId": "md-keychain-01",
      "version": 1,
      "format": "scad",
      "privateStorageKey": "production/porte-cles-prenom.scad",
      "sha256": "ff2f0a0b4bd651426cf0bb40b1ccaaf202522f4f6fcdf4341a5cc8d91a538f0d",
      "sourceType": "original",
      "sourceUrl": null,
      "creator": "Codex Builder for MustDesign3D",
      "licenceLabel": "Owner review pending; not a public downloadable asset",
      "permissions": {
        "commercialPrint": null,
        "modify": null,
        "redistribute": null
      },
      "reviewStatus": "needs_review",
      "rightsEvidenceRef": "README.md",
      "prototypeStatus": "unvalidated",
      "compiled": true,
      "slicedAt": null,
      "manufacturing": {
        "material": "PLA concept",
        "colorCount": 2,
        "filamentGrams": null,
        "purgeGrams": null,
        "printHours": null,
        "productionCostCents": null,
        "supportRequired": null
      },
      "geometryCheck": {
        "tool": "OpenSCAD 2021.01",
        "exportedAt": "2026-11-10",
        "stlVertices": 9552,
        "dimensionsMm": [
          75,
          28,
          3.6
        ],
        "exportRef": "exports/porte-cles-prenom.stl",
        "imageRef": "../public/models/porte-cles-prenom.png"
      }
    },
    {
      "id": "prototype-md-qr-01",
      "productId": "md-qr-01",
      "version": 1,
      "format": "scad",
      "privateStorageKey": "production/support-qr.scad",
      "sha256": "f709bdfe71c790dfaac089c7ba3f82f43fa307f9a87ef4a9f0c621feaeab59fb",
      "sourceType": "original",
      "sourceUrl": null,
      "creator": "Codex Builder for MustDesign3D",
      "licenceLabel": "Owner review pending; not a public downloadable asset",
      "permissions": {
        "commercialPrint": null,
        "modify": null,
        "redistribute": null
      },
      "reviewStatus": "needs_review",
      "rightsEvidenceRef": "README.md",
      "prototypeStatus": "unvalidated",
      "compiled": true,
      "slicedAt": null,
      "manufacturing": {
        "material": "PLA concept",
        "colorCount": 3,
        "filamentGrams": null,
        "purgeGrams": null,
        "printHours": null,
        "productionCostCents": null,
        "supportRequired": null
      },
      "geometryCheck": {
        "tool": "OpenSCAD 2021.01",
        "exportedAt": "2026-11-10",
        "stlVertices": 4368,
        "dimensionsMm": [
          90,
          55,
          125
        ],
        "exportRef": "exports/support-qr.stl",
        "imageRef": "../public/models/support-qr.png"
      }
    },
    {
      "id": "prototype-md-city-01",
      "productId": "md-city-01",
      "version": 1,
      "format": "scad",
      "privateStorageKey": "production/ville-maroc.scad",
      "sha256": "00add404e6ab8c80e4c237be8f5e2a2a18b1626216464a29e0fa5dbb78f61d2e",
      "sourceType": "original",
      "sourceUrl": null,
      "creator": "Codex Builder for MustDesign3D",
      "licenceLabel": "Owner review pending; not a public downloadable asset",
      "permissions": {
        "commercialPrint": null,
        "modify": null,
        "redistribute": null
      },
      "reviewStatus": "needs_review",
      "rightsEvidenceRef": "README.md",
      "prototypeStatus": "unvalidated",
      "compiled": true,
      "slicedAt": null,
      "manufacturing": {
        "material": "PLA concept",
        "colorCount": 3,
        "filamentGrams": null,
        "purgeGrams": null,
        "printHours": null,
        "productionCostCents": null,
        "supportRequired": null
      },
      "geometryCheck": {
        "tool": "OpenSCAD 2021.01",
        "exportedAt": "2026-11-10",
        "stlVertices": 12168,
        "dimensionsMm": [
          180,
          35,
          95
        ],
        "exportRef": "exports/ville-maroc.stl",
        "imageRef": "../public/models/ville-maroc.png"
      }
    },
    {
      "id": "prototype-md-pixel-01",
      "productId": "md-pixel-01",
      "version": 1,
      "format": "scad",
      "privateStorageKey": "production/plaque-pixel-zellige.scad",
      "sha256": "6eb045009b0f10ff31350cb0267b201fb86510e5b9c22a35381e62296a325ef1",
      "sourceType": "original",
      "sourceUrl": null,
      "creator": "Codex for MustDesign3D",
      "licenceLabel": "Owner review pending; not a public downloadable asset",
      "permissions": {
        "commercialPrint": null,
        "modify": null,
        "redistribute": null
      },
      "reviewStatus": "needs_review",
      "rightsEvidenceRef": "README.md",
      "prototypeStatus": "unvalidated",
      "compiled": true,
      "slicedAt": null,
      "manufacturing": {
        "material": "PLA concept",
        "colorCount": 3,
        "filamentGrams": null,
        "purgeGrams": null,
        "printHours": null,
        "productionCostCents": null,
        "supportRequired": null
      },
      "geometryCheck": {
        "tool": "OpenSCAD 2021.01",
        "exportedAt": "2026-11-10",
        "stlVertices": 564,
        "dimensionsMm": [
          86,
          86,
          3.6
        ],
        "exportRef": "exports/plaque-pixel-zellige.stl",
        "imageRef": "../public/models/plaque-pixel-zellige.png"
      }
    }
  ]
}
```

## Fichier production/plaque-bureau.scad

```scad
part = "assembly";
width = 160;
panel_height = 51;
panel_thickness = 3;
foot_depth = 45;
foot_height = 8;
slot_clearance = 0.4;
label_text = "Yasmine";
font_name = "Liberation Sans:style=Bold";
text_size = 15;
relief_height = 1;
$fn = 48;

assert(width <= 220 && panel_height <= 100 && foot_depth <= 100);
assert(slot_clearance > 0);

module panel_base() {
  color("#efdfc1") linear_extrude(panel_thickness) offset(r=3) square([width-6,panel_height-6],center=true);
}

module panel_lettering() {
  color("#233d99") translate([0,0,panel_thickness]) linear_extrude(relief_height)
    scale([min(1,(width-18)/max(1,len(label_text)*text_size*0.65)),1]) text(label_text,size=text_size,font=font_name,halign="center",valign="center");
}

module foot() {
  color("#d49b42") difference() {
    linear_extrude(foot_height) offset(r=3) square([width-6,foot_depth-6],center=true);
    translate([-width/2,-(panel_thickness+slot_clearance)/2,foot_height-4]) cube([width,panel_thickness+slot_clearance,5]);
  }
}

if (part == "foot" || part == "assembly") foot();
if (part == "panel-base") panel_base();
if (part == "panel-lettering") panel_lettering();
if (part == "panel") { panel_base(); panel_lettering(); }
if (part == "assembly") translate([0,panel_thickness/2,panel_height/2+foot_height-4]) rotate([90,0,0]) { panel_base(); panel_lettering(); }
```

## Fichier production/plaque-pixel-zellige.scad

```scad
part = "assembly";
pitch = 6;
rim = 10;
base_height = 2.6;
relief_height = 1;
base_color = "#efe3ca";
petal_color = "#233d99";
center_color = "#d49b42";
$fn = 40;

motif = [
  ".....B.....",
  "....BBB....",
  "..B.BBB.B..",
  "...BBBBB...",
  ".BBBAAABBB.",
  "BBBBAAABBBB",
  ".BBBAAABBB.",
  "...BBBBB...",
  "..B.BBB.B..",
  "....BBB....",
  ".....B....."
];
size = 11 * pitch + 2 * rim;

assert(pitch >= 4 && pitch <= 15);
assert(rim >= 5 && rim <= 20);
assert(base_height >= 2 && relief_height >= 0.6);

module outline() {
  hull() for (x = [4, size - 4], y = [4, size - 4]) translate([x, y]) circle(r=4);
}

module cells(symbol) {
  translate([rim, rim, base_height])
    linear_extrude(height=relief_height)
      for (row = [0:10], column = [0:10])
        if (motif[row][column] == symbol)
          translate([column * pitch, (10 - row) * pitch]) square(pitch);
}

if (part == "assembly" || part == "base") color(base_color) linear_extrude(height=base_height) outline();
if (part == "assembly" || part == "petals") color(petal_color) cells("B");
if (part == "assembly" || part == "center") color(center_color) cells("A");
```

## Fichier production/plaque-porte.scad

```scad
part = "assembly";
width = 150;
depth = 65;
base_height = 3;
relief_height = 1;
hole_diameter = 3.5;
label_text = "L'atelier";
font_name = "Liberation Sans:style=Bold";
text_size = 15;
$fn = 64;

assert(width <= 220 && depth <= 120 && base_height+relief_height <= 4);

module outline(inset=0) {
  hull() for (horizontal = [-width/2+depth/2,width/2-depth/2]) translate([horizontal,0]) circle(r=depth/2-inset);
}

module holes() {
  for (horizontal = [-width/2+10,width/2-10]) translate([horizontal,0,-1]) cylinder(h=base_height+relief_height+2,d=hole_diameter);
}

module base() {
  color("#efdfc1") difference() { linear_extrude(base_height) outline(); holes(); }
}

module border() {
  color("#d49b42") difference() {
    translate([0,0,base_height]) linear_extrude(relief_height) difference() { outline(4); outline(5.5); }
    holes();
  }
}

module lettering() {
  color("#233d99") translate([0,0,base_height]) linear_extrude(relief_height)
    scale([min(1,(width-38)/max(1,len(label_text)*text_size*0.65)),1]) text(label_text,size=text_size,font=font_name,halign="center",valign="center");
}

if (part == "base" || part == "assembly") base();
if (part == "border" || part == "assembly") border();
if (part == "lettering" || part == "assembly") lettering();
```

## Fichier production/porte-cles-prenom.scad

```scad
part = "assembly";
width = 75;
depth = 28;
base_height = 2.6;
relief_height = 1;
hole_diameter = 5;
french_name = "Meryem";
arabic_name = "";
font_name = "Liberation Sans:style=Bold";
text_size = 10;
base_color = "#efdfc1";
text_color = "#233d99";
$fn = 64;

assert(width >= 65 && width <= 85);
assert(depth >= 24 && depth <= 40);
assert(base_height + relief_height <= 4);

module rounded_outline() {
  hull() for (position = [[-width/2+7,-depth/2+7], [width/2-7,-depth/2+7], [-width/2+7,depth/2-7], [width/2-7,depth/2-7]]) translate(position) circle(r=7);
}

module base() {
  color(base_color) difference() {
    linear_extrude(base_height) rounded_outline();
    translate([-width/2+7,0,-1]) cylinder(h=base_height+2,d=hole_diameter);
  }
}

module label_line(label_text, vertical_offset) {
  translate([4,vertical_offset,base_height]) linear_extrude(relief_height)
    scale([min(1,(width-22)/max(1,len(label_text)*text_size*0.65)),1]) text(label_text,size=text_size,font=font_name,halign="center",valign="center");
}

module lettering() {
  color(text_color) {
    label_line(french_name,arabic_name == "" ? 0 : 6);
    if (arabic_name != "") label_line(arabic_name,-6);
  }
}

if (part == "base" || part == "assembly") base();
if (part == "lettering" || part == "assembly") lettering();
```

## Fichier production/support-qr.scad

```scad
part = "assembly";
panel_width = 90;
panel_height = 121;
panel_thickness = 3;
foot_depth = 55;
foot_height = 8;
slot_clearance = 0.4;
placeholder_size = 61;
$fn = 48;

assert(panel_width <= 220 && panel_height+foot_height <= 220 && foot_depth <= 220);

module panel_base() {
  color("#efdfc1") linear_extrude(panel_thickness) offset(r=4) square([panel_width-8,panel_height-8],center=true);
}

module non_scannable_qr_placeholder() {
  color("#233d99") translate([0,0,panel_thickness]) linear_extrude(1) difference() {
    square([placeholder_size,placeholder_size],center=true);
    square([placeholder_size-6,placeholder_size-6],center=true);
  }
  color("#233d99") translate([0,0,panel_thickness]) linear_extrude(1) {
    rotate(45) square([24,24],center=true);
    translate([0,-43]) text("DEMO",size=8,font="Liberation Sans:style=Bold",halign="center");
  }
}

module foot() {
  color("#d49b42") difference() {
    linear_extrude(foot_height) offset(r=3) square([panel_width-6,foot_depth-6],center=true);
    translate([-panel_width/2,-(panel_thickness+slot_clearance)/2,foot_height-4]) cube([panel_width,panel_thickness+slot_clearance,5]);
  }
}

if (part == "foot" || part == "assembly") foot();
if (part == "panel-base") panel_base();
if (part == "placeholder") non_scannable_qr_placeholder();
if (part == "panel") { panel_base(); non_scannable_qr_placeholder(); }
if (part == "assembly") translate([0,panel_thickness/2,panel_height/2+foot_height-4]) rotate([90,0,0]) { panel_base(); non_scannable_qr_placeholder(); }
```

## Fichier production/ville-maroc.scad

```scad
part = "assembly";
width = 180;
foot_depth = 35;
foot_height = 8;
silhouette_height = 87;
silhouette_thickness = 4;
city_text = "Marrakech";
font_name = "Liberation Sans:style=Bold";
text_size = 12;
$fn = 48;

assert(width <= 220 && silhouette_height+foot_height <= 220 && foot_depth <= 100);

module skyline_placeholder_outline() {
  difference() {
    union() {
      translate([-width/2,0]) square([width,32]);
      translate([-width/2+8,0]) square([32,52]);
      translate([-width/2+42,0]) square([28,68]);
      translate([width/2-55,0]) square([32,58]);
      translate([17,0]) square([18,silhouette_height]);
      translate([13,silhouette_height-7]) square([26,7]);
    }
    translate([-40,0]) union() { square([22,22]); translate([11,22]) circle(r=11); }
    translate([49,0]) union() { square([15,17]); translate([7.5,17]) circle(r=7.5); }
  }
}

module silhouette() {
  color("#efdfc1") linear_extrude(silhouette_thickness) skyline_placeholder_outline();
}

module foot_base() {
  color("#233d99") translate([-width/2,-foot_depth/2,0]) cube([width,foot_depth,foot_height]);
}

module city_lettering() {
  color("#d49b42") translate([0,-foot_depth/2+7,foot_height]) linear_extrude(1)
    scale([min(1,(width-16)/max(1,len(city_text)*text_size*0.65)),1]) text(city_text,size=text_size,font=font_name,halign="center",valign="center");
}

if (part == "foot" || part == "assembly") foot_base();
if (part == "lettering" || part == "assembly") city_lettering();
if (part == "silhouette") silhouette();
if (part == "assembly") translate([0,4,foot_height]) rotate([90,0,0]) silhouette();
```

## Fichier prompts/00-master-mustdesign3d.md

```markdown
# Prompt maître MustDesign3D

## Mission

Tu es l’agent de développement de MustDesign3D, marque marocaine d’objets personnalisés imprimés en 3D. Travaille dans le projet Next.js existant. Lis codex.md, le README des prompts et les documents de recherche avant le prompt du jalon demandé.

Les nouveaux fichiers de ce dossier précisent l’évolution du site. Le PDF Master Prompt sert de référence pour le parcours commercial. Les besoins retenus sont les cadeaux et objets de bureau au Maroc, le français, la personnalisation arabe et la devise MAD.

## État de départ à préserver

Le projet possède déjà /, /shop, /contact et /product/[slug], six produits locaux, un aperçu prénom français/arabe/bilingue et un panier latéral démo en mémoire. Lire le code réel avant de modifier un comportement. Réutiliser les composants adaptés et les URLs.

Utiliser Next.js App Router, React, TypeScript strict et Tailwind selon le package-lock.json. Les versions changent uniquement si un besoin vérifié le justifie.

## Nouvelle expérience

1. Présenter une marque identifiable MustDesign3D, avec un accueil visuel, trois produits vedettes et quatre collections.
2. Donner une recherche et des filtres utilisables sur mobile.
3. Faire de chaque fiche un parcours complet avec détails, options applicables, prix indicatif et produits associés.
4. Proposer un panier latéral qui conserve les choix et se restaure après rechargement en démo.
5. Présenter une barre de contact et une page projet adaptées à l’atelier.
6. Séparer les modèles en recherche des produits réellement validés pour la boutique.

Direction graphique initiale retenue pour cette itération, fond ivoire, sable, anthracite, accent Majorelle, détails géométriques sobres et photos produit dominantes. Adapter la composition à MustDesign3D avec une copie française originale.

## Catalogue et modèles

Consulter les références To7fa et 3DGIFI pour la structure de catalogue et les usages. Consulter SliSearch pour découvrir des fichiers et retrouver leurs créateurs.

L’inventaire de liens sert à la recherche. Acquérir un modèle auprès de sa source primaire et enregistrer ses droits d’impression commerciale, de modification et de redistribution. Vérifier séparément les images, le logo, les polices et les éléments de marque. Les modèles inconnus restent en recherche. Préparer des designs originaux quand le besoin est simple.

L’A1 et son AMS Lite donnent le cadre du projet, jusqu’à quatre couleurs simultanées, PLA prioritaire, géométrie simple et support limité. Pour les prototypes de départ, viser 220 × 220 × 220 mm au maximum et préférer deux ou trois couleurs. Les estimations de poids, temps, purge et marge sont renseignées après slicing ou clairement identifiées comme hypothèses.

Le catalogue démo conserve ses six produits et leurs prix indicatifs. Les trois vedettes sont le porte-clés prénom, la plaque de bureau et le support QR. Les autres candidats passent les vérifications du registre avant publication.

## Modes de fonctionnement

- Démo par défaut, parcours visuel et panier interactifs, message « Commandes bientôt disponibles » avant collecte de coordonnées.
- Les futurs POST commandes et devis refusent les écritures en mode démo avant lecture du corps de requête et avant connexion à PostgreSQL.
- Les coordonnées réelles de MustDesign3D seront fournies par le propriétaire. Une valeur absente donne un état d’attente clair.
- Le prochain jalon commandes utilise PostgreSQL local et des données synthétiques pour les essais.
- La publication Railway intervient après la demande explicite du propriétaire. Le guide contient les étapes à suivre à ce moment.

## Qualité et fin de jalon

Garder les composants lisibles, séparer UI cliente, catalogue public et données internes. Maintenir les noms arabes en Unicode, utiliser dir="auto" et les propriétés logiques. Prévoir états vide/chargement/erreur, 404 produit et contrôle clavier.

Tester le comportement changé, puis TypeScript et le build. Rapporter les vérifications réellement exécutées et les tâches restantes. Une licence déclarée par un agrégateur reste à vérifier chez le créateur. Un aperçu 2D valide la composition visuelle, la fabrication se valide dans le slicer puis sur prototype.

Remettre un résultat local reviewable avec les fichiers concernés. Conserver les prix démonstratifs identifiables jusqu’à validation de l’atelier.
```

## Fichier prompts/05-plan-refonte-niches-et-photos.md

```markdown
# Plan de refonte MustDesign3D — niches, produits et photographie

Document du 10 novembre 2026. Plan préparé à partir du rapport Morocco_3D_Printing_Niche_Research_Report.docx, du guide MakerWorld_Guide.pdf, du PDF All our pieces · To7fa et du catalogue To7fa consulté avec Search Service. La capture jointe montre les deux gabarits actuellement exposés dans la boutique.

## 1. Décisions de départ

### Positionnement

MustDesign3D devient une marque marocaine de personnalisation, centrée sur les cadeaux nominatifs et les objets utiles à la présentation d’une petite entreprise. Les collections sont Cadeaux personnalisés, Maison & bureau et Pour les professionnels.

Le rapport apporte une recherche documentaire et des hypothèses de lancement. Les fiches concurrentes confirment des offres et des prix affichés. Les ventes, volumes de demande et marges MustDesign3D restent à mesurer auprès de clients et sur les prototypes.

### Hypothèses retenues en attendant le retour du propriétaire

- Neuf références pour la première collection, puis trois extensions après tests.
- Français au lancement, personnalisation arabe et bilingue conservée.
- Filaments noir, blanc, bleu et rouge, selon le rapport et A1_100_Product_References.md.
- Habillage de marque ivoire et sable avec accent bleu Majorelle. Ces couleurs d’interface sont indépendantes des filaments proposés.
- Concepts visuels IA pour la démonstration, puis photographies des prototypes validés pour la vente.
- Site local et commandes fermées pendant cette refonte.

Les questions sur la sélection et les photos ont été envoyées au propriétaire. Une réponse différente conduit à réviser ces hypothèses avant l’implémentation.

### Ce que la référence To7fa apporte

Reprendre les principes observés, recherche visible, filtres latéraux, grille dense, images en situation, prix lisibles, pastilles de couleur et fiche personnalisable. Préparer les textes, objets et médias propres à MustDesign3D. [Catalogue To7fa](https://to7fa.ma/en/products)

Les deux rendus de la capture actuelle représentent un gabarit QR et un monogramme provisoire. Le travail de refonte porte sur leur conception, leur contenu, leur présentation et leur classement dans le catalogue. Un changement d’éclairage seul laisserait ces limites visibles.

## 2. Les trois niches et les neuf produits

Les prix ci-dessous sont des hypothèses de test pour le catalogue démo. Le passage à un prix commercial dépend du coût réel, du temps de machine, de l’emballage et de la livraison.

| Collection / clientèle | Produit à développer | Différenciation MustDesign3D | Prix démo proposé |
| --- | --- | --- | --- |
| Cadeaux personnalisés / particuliers | Porte-clés prénom en contour | Prénom latin ou arabe, base épousant la silhouette du texte, anneau renforcé | 49 MAD |
| Cadeaux personnalisés / particuliers | Porte-clés plaque marocaine | Composition lisible, numéros et lettre choisis, deux couleurs | 45 MAD |
| Cadeaux personnalisés / particuliers | Étiquette de sac | Prénom, choix d’un pictogramme original et fixation adaptée | 39 MAD |
| Cadeaux personnalisés / événements | Marque-places nominatifs | Lot de dix prénoms, typographie cohérente et série imprimée à plat | Sur devis pour le lot |
| Maison & bureau / particuliers et indépendants | Plaque prénom de bureau | Nom et fonction avec proportions typographiques contrôlées | 99 MAD |
| Maison & bureau / particuliers | Plaque de porte | Nom de famille ou pièce, deuxième ligne et fixation choisie | 99 MAD |
| Professionnels / cafés, salons et commerces | Présentoir QR | Véritable QR lié à un menu, une page ou une demande d’avis, socle stable | 149 MAD |
| Professionnels / commerces et indépendants | Plaque de contact | Enseigne compacte avec nom et identifiant social, présentation murale ou de comptoir | 99 MAD |
| Professionnels / petites séries | Porte-clés logo en lot | Géométrie simplifiée après accord du client et estimation par quantité | Sur devis |

Les quatre premiers produits sont personnalisables rapidement à partir de gabarits. Les présentoirs et petites séries visent des paniers plus élevés, avec un délai d’étude à mesurer.

### Priorité de prototypage et de présentation

Commencer par trois produits vedettes, le porte-clés prénom, la plaque de bureau et le présentoir QR. Faire approuver leur forme et une direction photo avant d’étendre la production d’images aux neuf références.

Le guide MakerWorld décrit un modèle paramétrique d’Alberto Nicás, version 2.9, avec modes simple face et double face en deux moitiés collées. Le PDF fourni décrit son fonctionnement. Le fichier source correspondant et ses conditions d’utilisation restent à obtenir. Une implémentation MustDesign3D peut être dessinée à partir du besoin fonctionnel avec une provenance propre.

### Références de prix observées

- Un porte-clés prénom est affiché à 35 MAD chez To7fa. La fiche présente notamment les graphies latines/arabe et le choix des couleurs. [Fiche To7fa](https://to7fa.ma/produits/porte-cles-prenom)
- Une plaque de porte est affichée à 79 MAD chez To7fa. [Fiche To7fa](https://to7fa.ma/produits/plaque-de-porte-classique)
- Un présentoir avec QR et NFC est affiché à 149 MAD chez To7fa. Comparer les fonctions et composants au moment du chiffrage MustDesign3D. [Fiche To7fa](https://to7fa.ma/en/products/presentoir-avis-nfc-qr)
- Un porte-clés de plaque marocaine est affiché à 50 MAD chez Slowy Wear au moment de la consultation. [Fiche Slowy Wear](https://slowywear.ma/product/porte-cle-immatriculation-marocaine-personnalise/)

### Extensions après le premier test

Étudier un porte-crayons nommé, un support téléphone simple et un ensemble de repères de câbles. Ces références enrichissent l’usage bureau lorsque les premiers produits ont une fabrication et une marge mesurées.

La skyline et la plaque pixel existantes passent dans une collection de prototypes. Le présentoir de logo se présente comme projet sur mesure avec un exemple typographique MustDesign3D. Leur visibilité commerciale dépend de la validation d’un modèle et d’un visuel approuvés.

## 3. Concevoir des produits représentables fidèlement

### Gabarits à corriger ou créer

1. Porte-clés prénom, base en contour, largeur nominale autour de 75 mm, œillet relié et renforcé, texte en relief sur une hauteur commune pour limiter les changements de couleur. Préparer une version simple face en premier.
2. Plaque marocaine et étiquette de sac, géométries plates indépendantes, proportions définies et fixation testée.
3. Plaques bureau/porte, noms et fonctions réellement lisibles, support et panneau séparables, proportions validées à l’échelle.
4. Présentoir QR, panneau noir/blanc contrasté sur socle bleu ou noir, vrai code généré depuis le lien saisi. Tester la lecture sur écran puis sur l’objet imprimé avant vente. Le NFC constitue une extension matérielle à chiffrer et tester.
5. Plaque de contact, vrai texte de démonstration choisi par MustDesign3D et identifiant clairement fictif.
6. Petites séries, gabarits de marque-places et porte-clés logo, liste de noms et coût de lot séparés du prix unitaire.

Pour les premiers modèles, viser deux couleurs et au plus trois changements réellement comptés dans le slicer lorsque la géométrie par couches le permet. Si une pièce demande de nombreux changements, préparer des composants monochromes et mesurer le temps d’assemblage.

### Vérification des modèles

- Enveloppe conservatrice de 220 mm, avec place pour les éléments de slicing.
- Buse 0,4 mm et couches 0,20 mm comme point de départ des essais.
- Contrôle des îlots, des lettres fines et des points de fixation.
- Validation de la liaison des lettres arabes avec une police autorisée et un tracé correctement façonné.
- Export des parties, slicing sur le profil A1, relevé matière utile/purge/temps, puis impression d’essai.
- Pour la double face du guide, prévoir les deux demi-bases, la correspondance des trous et le contrôle de la lecture après retournement et collage. Cette option s’ajoute après validation du simple face.

Chaque modèle possède une version, une provenance, les permissions nécessaires, ses dimensions et un résultat de prototype. La liste de cent références reste un outil de découverte. Les permissions et la géométrie se contrôlent fichier par fichier.

## 4. Nouvelle direction photo

### Style retenu

Lumière naturelle douce, ombres de contact, plastique mat avec stries fines cohérentes avec le FDM, échelle crédible et accessoires sobres. Décors secondaires possibles, bois clair, papier, tissu écru et comptoir de café. Le produit reste le point focal et ses couleurs correspondent aux filaments disponibles.

Le PDF To7fa sert de référence de mise en scène et de cadrage. Les images MustDesign3D montrent ses propres objets et personnalisations.

### Trois vues par référence

- Vue principale en situation, cadrage 4:5 pour la carte catalogue.
- Packshot sur fond ivoire, cadrage 1:1, proportions et détails visibles.
- Vue de détail ou d’échelle, cadrage 4:3, nom et assemblage lisibles.

Pour neuf références, prévoir vingt-sept images finales, puis une image d’accueil et trois vues de collection, soit trente et un médias. Produire ce volume après validation du premier essai.

### Première passe de validation

1. Choisir les modèles corrigés du porte-clés et du présentoir QR.
2. Produire une image conceptuelle de chacun avec le modèle corrigé comme référence géométrique.
3. Comparer au fichier de référence, contour, œillet, épaisseurs, textes, nombre de couleurs et socle.
4. Corriger la direction de prise de vue ou le modèle selon le problème observé.
5. Après accord sur cette paire, compléter les trois vues des trois vedettes, puis les six autres références.

### Utilisation possible de Gemini

Une intégration Gemini de génération d’images est disponible via le connecteur Runway dans cette session. À l’étape d’exécution, vérifier le compte, les crédits et le modèle disponible avant le lot pilote. Le présent plan n’engage aucune génération d’image.

Employer l’image du modèle corrigé ou la photo du prototype comme référence. Préserver le produit pendant le changement de décor et de lumière. Le texte, les logos et le QR doivent rester contrôlables, avec reprise du graphisme approuvé lorsque la génération les altère.

Les images de synthèse portent la mention « Visualisation du concept ». Les photos de prototypes validés remplacent progressivement les vues commerciales correspondantes. Une photo générée à partir d’un gabarit provisoire reste une représentation de ce gabarit.

### Exemple de prompt pour le lot pilote

> À partir de la référence du porte-clés MustDesign3D, conserver exactement son contour, son œillet, ses proportions, son épaisseur et son prénom approuvé. Présenter le produit en plastique FDM mat noir avec lettres blanches, posé sur une petite coupelle en bois clair près de clés métalliques. Lumière de fenêtre douce, ombre de contact réaliste, stries d’impression fines, vue trois-quarts, cadrage 4:5. Le produit occupe la majorité de l’image. Conserver les détails de la référence et la même palette de deux filaments.

### Contrôle des médias

Associer chaque image à productId, modelVersion, type de média et couleurs représentées. Vérifier les noms arabes visuellement, la cohérence entre les vues et la fidélité au prototype. Conserver une provenance distincte pour les médias et les fichiers 3D.

Export WebP/AVIF avec dimensions adaptées, 1 600 px pour les fiches et 2 400 px pour le visuel principal si nécessaire. Viser 150–250 Ko par image catalogue lorsque la qualité le permet, et conserver les sources haute définition séparément.

## 5. Refaire le catalogue et les fiches

### Structure du catalogue

- En-tête MustDesign3D compact, navigation claire, contact et panier.
- Titre de collection, nombre de produits et tri visibles.
- À partir de 1 440 px, barre de filtres d’environ 220 px et grille de quatre cartes.
- Sur écran intermédiaire, grille de trois cartes lorsque l’espace le permet.
- Sur mobile, filtres dans un panneau accessible et grille de deux cartes dès 360 px. Prévoir une colonne sur les plus petits écrans.
- Filtres par collection, type de produit, couleur réellement disponible, personnalisation et fourchette de prix.
- Cartes avec image 4:5 cohérente, nom court, prix indicatif ou devis, pastilles de couleur et action « Personnaliser ».
- Recherche, tri et filtres conservés dans l’URL avec navigation arrière fonctionnelle.

La bibliothèque technique /modeles devient un espace secondaire de consultation des prototypes. Les cartes de la boutique utilisent la nouvelle direction photo, avec leur statut de média explicite. Le personnage flottant de la capture appartient à l’interface hôte et reste extérieur aux compositions produit.

### Fiche produit

Prévoir une galerie de trois vues, les options adaptées au produit, un aperçu contrôlé, les dimensions validées ou indicatives, une quantité et un récapitulatif. Pour les lots, afficher le nombre de pièces et demander les noms ou le besoin de logo de façon explicite.

La personnalisation QR ajoute le nom du commerce, le type de destination et le lien. Encoder le code localement et conserver sa zone calme. Vérifier le décodage avant d’accepter une composition pour fabrication.

La version double face du porte-clés possède ses propres champs et son aperçu de face/dos. Préserver les saisies actuelles lors de l’évolution du contrat et revalider les anciennes compositions avec une explication si une nouvelle limite s’applique.

### Changements de données

- Garder les identifiants et slugs existants pour les produits conservés.
- Ajouter les nouvelles références avec identifiants stables et une distinction entre référence et variante.
- Ajouter pricingMode=fixed ou quote. Conserver priceCents entier pour les prix fixes et utiliser null pour les devis. Les cartes, fiches et API affichent « Sur devis » pour ces références. Une valeur nulle ne donne jamais un prix à zéro.
- Conserver les trois collections principales avec les categoryId existants adaptés, et afficher Décoration dans l’espace des essais.
- Compléter ProductImage par un type photo, generated-concept ou cad-preview, une provenance et la version du modèle représenté. Prévoir une conversion des anciennes lignes contenant isDemo.
- Séparer les images commerciales, les aperçus de personnalisation et les fichiers privés de production.
- Prévoir les palettes par produit et par stock de filaments. Le bleu, noir, blanc et rouge constituent la première hypothèse.
- Faire évoluer les contrats de panier de manière versionnée, avec conservation/revalidation des saisies existantes.

Les principaux points d’entrée du code sont le catalogue serveur, la carte produit et le composant de média. La refonte réutilise les parcours de personnalisation et de panier déjà testés.

## 6. Ordre d’exécution et critères de validation

### Lot 1 — Cadrage commercial

Valider les neuf références, les couleurs disponibles, les formes des trois vedettes et les prix de démonstration. Pour la demande réelle, fixer comme objectif interne vingt échanges qualifiés avec des acheteurs potentiels et cinq demandes de devis. Ces valeurs sont des objectifs de test.

### Lot 2 — Modèles et preuves

Corriger les modèles des trois vedettes, vérifier les sources/licences/polices, exporter les parties et mesurer les coûts dans Bambu Studio. Photographier les premières impressions lorsqu’elles sont disponibles.

### Lot 3 — Direction photo

Créer la paire de visuels pilote, l’évaluer avec les références, puis produire le reste de la série après approbation. En cas de compte de génération indisponible, préparer les prompts et les références pour une exécution par le propriétaire.

### Lot 4 — Refonte locale

Adapter la grille, les filtres, les galeries et les contrats de médias. Ajouter les nouveaux produits et options. Rétablir les anciennes compositions du panier selon la migration prévue.

### Lot 5 — Recette

- Chaque référence a un visuel approuvé, une provenance et un statut de fabrication explicite.
- Le QR de démonstration se décode vers son lien exact. La lecture sur objet imprimé sera vérifiée séparément.
- Les textes français/arabe et les couleurs concordent entre le formulaire, les images de référence et le panier.
- Les cartes et filtres sont utilisables à 320, 390, 768, 1 024 et 1 440 px.
- Navigation clavier, focus du panneau de filtres et du panier, retour arrière et anciennes compositions vérifiés.
- TypeScript, build et recette navigateur réussis.
- Coût réel et gain par heure de machine calculés avant publication commerciale.

La sortie de cette phase est une nouvelle vitrine locale reviewable. La génération automatique de fichiers de production depuis une commande, l’administration complète, les paiements et la publication Railway appartiennent aux étapes suivantes.

## Sources de travail

- [Rapport de niches fourni](C:/Users/mekka/Downloads/Morocco_3D_Printing_Niche_Research_Report.docx)
- [Guide MakerWorld fourni](C:/Users/mekka/Downloads/MakerWorld_Guide.pdf)
- [PDF catalogue fourni](C:/Users/mekka/Desktop/All%20our%20pieces%20%C2%B7%20To7fa.pdf)
- [Liste interne de cent références](A1_100_Product_References.md)
- [Brief MustDesign3D](00-master-mustdesign3d.md)

Le texte annoncé « Pasted text #1 » n’apparaît pas comme pièce textuelle distincte dans les éléments reçus. Le plan s’appuie sur la capture jointe, les trois documents accessibles et le brief existant.
```

## Fichier prompts/A1_100_Product_References.md

```markdown
# 100 product references — Bambu Lab A1 / AMS Lite

Research date: 10 November 2026. Palette: black, white, blue, red.

## What this list contains

60 items in the observed To7fa catalogue order, followed by 40 distinct 3DGIFI references from accessible shop pages. This is a research selection, not a combined “first 100” order, sales ranking, or 100 validated printable files. Some 3DGIFI retrievals are cached and catalogue totals differ between snapshots. Product names are shortened identifiers; photos and descriptions are not copied.

Each source link is a physical-product reference. The model-search links are prepared queries for finding similar files, NOT verified downloads of the shop's exact design. A search can return no match. Neither shop's public catalogue establishes permission to reproduce its designs or reuse its photos.

## Print and licence gate

- FIRST = promising concept for an initial prototype, not an approved STL. TEST = evaluate after simple products. HOLD = defer from the simple starter range.
- All 100 rows: model author UNKNOWN; exact STL/3MF UNKNOWN; commercial printing licence UNKNOWN; modification permission UNKNOWN; redistribution permission UNKNOWN; dimensions UNKNOWN unless an explicit advertised-size warning is recorded. No model has passed the acceptance gate.
- Actual supports, flat base, floating details, wall thickness, tool changes, filament weight, purge and time are UNKNOWN until an exact file is opened and sliced. Colour schemes and methods below are proposed adaptations, not observed manufacturing instructions.
- The A1 build volume is 256 × 256 × 256 mm; 220 mm is your conservative project limit. Start under 150 mm where practical. Include brim/purge-tower space when validating fit.
- Start with PLA, 0.4 mm nozzle and 0.2 mm layers as trial settings. AMS mapping: 1 black, 2 white, 3 blue, 4 red. Profile settings still depend on filament and model.
- For a layer-coloured design, base and raised text must occupy separate heights. Four colours do not imply three changes: colours repeated on each layer can cause many swaps. Check the sliced tool-change count.
- For separate components, use monochrome batches: zero automatic colour swaps within each batch, then assemble. This is suitable for pixel tiles, with a tolerance test for the grid.
- Accept only after confirming ≤4 palette colours, ≤3 actual swaps, no supports, stable flat base, no unsupported tiny islands, fit within the chosen envelope, and a successful test print. Verify commercial printing, modification and redistribution separately on the creator's page.

## The complete list

The search columns target MakerWorld and Printables. Use the exact query on SliSearch, Cults3D or Thangs as an alternative. They are similar-model searches, not a claim of identical or commercially licensed files.

| # | Product reference | Shop | Observed shop price | Priority | Suggested palette | Proposed colour method | Similar-model search | Main check |
|---|---|---|---|---|---|---|---|---|
| 001 | [Porte-Clés Prénom Bulle](https://to7fa.ma/produits/porte-cles-prenom-bulle) | To7fa | 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=bubble%20name%20keychain) · [Printables](https://www.printables.com/search/models?q=bubble%20name%20keychain) | Use a flat-backed version; check thin strokes and ring strength. |
| 002 | [Porte-clés Plaque d'Immatriculation](https://to7fa.ma/produits/porte-cles-plaque-immatriculation) | To7fa | 35 MAD | FIRST | White + black | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=license%20plate%20keychain%20customizable) · [Printables](https://www.printables.com/search/models?q=license%20plate%20keychain%20customizable) | Use a flat-backed version; check thin strokes and ring strength. |
| 003 | [Porte-clés prénom à bordure](https://to7fa.ma/produits/porte-cles-prenom-a-bordure) | To7fa | 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=border%20name%20keychain) · [Printables](https://www.printables.com/search/models?q=border%20name%20keychain) | Use a flat-backed version; check thin strokes and ring strength. |
| 004 | [Porte-Clés Prénom et Cœur](https://to7fa.ma/produits/porte-cles-prenom-et-c-ur) | To7fa | 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=heart%20name%20keychain) · [Printables](https://www.printables.com/search/models?q=heart%20name%20keychain) | Use a flat-backed version; check thin strokes and ring strength. |
| 005 | [Prénom en Lettres Bulles](https://to7fa.ma/produits/prenom-lettres-bulles) | To7fa | 19 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=freestanding%20bubble%20letters) · [Printables](https://www.printables.com/search/models?q=freestanding%20bubble%20letters) | Use a flat-backed version; check thin strokes and ring strength. |
| 006 | [Porte-clés Prénom Marguerite](https://to7fa.ma/produits/porte-cles-prenom-marguerite) | To7fa | 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=flower%20name%20keychain) · [Printables](https://www.printables.com/search/models?q=flower%20name%20keychain) | Use a flat-backed version; check thin strokes and ring strength. |
| 007 | [Porte-clés prénom](https://to7fa.ma/produits/porte-cles-prenom) | To7fa | 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=customizable%20name%20keychain) · [Printables](https://www.printables.com/search/models?q=customizable%20name%20keychain) | Use a flat-backed version; check thin strokes and ring strength. |
| 008 | [Porte-clés Prénom Gonflé 3D](https://to7fa.ma/produits/porte-cles-prenom-gonfle-3d) | To7fa | 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=puffy%20name%20keychain) · [Printables](https://www.printables.com/search/models?q=puffy%20name%20keychain) | Use a flat-backed version; check thin strokes and ring strength. |
| 009 | [Perles Oursons Lettres](https://to7fa.ma/produits/perles-oursons-lettres) | To7fa | 35 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=bear%20alphabet%20beads) · [Printables](https://www.printables.com/search/models?q=bear%20alphabet%20beads) | Geometry, dimensions and supports unknown until file inspection. |
| 010 | [Organiseur Prénom Cœur](https://to7fa.ma/produits/organiseur-prenom-c-ur) | To7fa | 75 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=heart%20desk%20organizer%20personalized) · [Printables](https://www.printables.com/search/models?q=heart%20desk%20organizer%20personalized) | Geometry, dimensions and supports unknown until file inspection. |
| 011 | [Porte-clés Prénom en Relief](https://to7fa.ma/produits/porte-cles-prenom-en-relief) | To7fa | 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=raised%20text%20keychain) · [Printables](https://www.printables.com/search/models?q=raised%20text%20keychain) | Use a flat-backed version; check thin strokes and ring strength. |
| 012 | [Prénoms pour dragées (lot)](https://to7fa.ma/produits/prenoms-pour-dragees) | To7fa | dès 49 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=wedding%20favor%20name%20tags) · [Printables](https://www.printables.com/search/models?q=wedding%20favor%20name%20tags) | Use a flat-backed version; check thin strokes and ring strength. |
| 013 | [Étui Briquet Graphique](https://to7fa.ma/produits/etui-briquet-graphique) | To7fa | 35 MAD | HOLD | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=lighter%20sleeve%20geometric) · [Printables](https://www.printables.com/search/models?q=lighter%20sleeve%20geometric) | Fit and heat exposure require evaluation; not an initial PLA product. |
| 014 | [Étui Capsule pour Briquet](https://to7fa.ma/produits/etui-capsule-pour-briquet) | To7fa | 49 MAD | HOLD | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=lighter%20capsule%20case) · [Printables](https://www.printables.com/search/models?q=lighter%20capsule%20case) | Fit and heat exposure require evaluation; not an initial PLA product. |
| 015 | [Perles Lettres Personnalisées](https://to7fa.ma/produits/perles-lettres-personnalisees) | To7fa | 35 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=alphabet%20beads) · [Printables](https://www.printables.com/search/models?q=alphabet%20beads) | Geometry, dimensions and supports unknown until file inspection. |
| 016 | [Initiales pour dragées (lot)](https://to7fa.ma/produits/initiales-pour-dragees) | To7fa | dès 29 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=wedding%20favor%20initials) · [Printables](https://www.printables.com/search/models?q=wedding%20favor%20initials) | Use a flat-backed version; check thin strokes and ring strength. |
| 017 | [Porte-encens Onde Pure](https://to7fa.ma/produits/porte-encens-onde-pure) | To7fa | 35 MAD | HOLD | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=wave%20incense%20holder) · [Printables](https://www.printables.com/search/models?q=wave%20incense%20holder) | Do not expose PLA to embers or flame; redesign as decorative-only or assess a heat-resistant insert. |
| 018 | [Lettre de Naissance Personnalisée](https://to7fa.ma/produits/lettre-de-naissance-personnalisee) | To7fa | 139 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=birth%20announcement%20letter) · [Printables](https://www.printables.com/search/models?q=birth%20announcement%20letter) | Use a flat-backed version; check thin strokes and ring strength. |
| 019 | [Porte-clés Plaque Européenne](https://to7fa.ma/produits/porte-cles-plaque-europeenne) | To7fa | 35 MAD | FIRST | White + black | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=European%20license%20plate%20keychain) · [Printables](https://www.printables.com/search/models?q=European%20license%20plate%20keychain) | Use a flat-backed version; check thin strokes and ring strength. |
| 020 | [Boucles Fleur de Cerisier](https://to7fa.ma/produits/boucles-fleur-de-cerisier) | To7fa | dès 19 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=cherry%20blossom%20earrings) · [Printables](https://www.printables.com/search/models?q=cherry%20blossom%20earrings) | Fine details and attachment holes need a test; add suitable earring hardware. |
| 021 | [Organisateur Côtelé pour Télécommandes](https://to7fa.ma/produits/organisateur-cotele-pour-telecommandes) | To7fa | 79 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=ribbed%20remote%20control%20organizer) · [Printables](https://www.printables.com/search/models?q=ribbed%20remote%20control%20organizer) | Geometry, dimensions and supports unknown until file inspection. |
| 022 | [Porte-clés disque de fonte](https://to7fa.ma/produits/porte-cles-disque-de-fonte) | To7fa | 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=weight%20plate%20keychain) · [Printables](https://www.printables.com/search/models?q=weight%20plate%20keychain) | Use a flat-backed version; check thin strokes and ring strength. |
| 023 | [Porte-Clés Initiale et Prénom](https://to7fa.ma/produits/porte-cles-initiale-et-prenom) | To7fa | 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=initial%20name%20keychain) · [Printables](https://www.printables.com/search/models?q=initial%20name%20keychain) | Use a flat-backed version; check thin strokes and ring strength. |
| 024 | [Porte-clés Prénom Double Contour](https://to7fa.ma/produits/porte-cles-prenom-double-contour) | To7fa | 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=double%20border%20name%20keychain) · [Printables](https://www.printables.com/search/models?q=double%20border%20name%20keychain) | Use a flat-backed version; check thin strokes and ring strength. |
| 025 | [Porte-clés Maillot de Foot](https://to7fa.ma/produits/porte-cles-maillot-de-foot) | To7fa | 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=football%20shirt%20keychain) · [Printables](https://www.printables.com/search/models?q=football%20shirt%20keychain) | Use a flat-backed version; check thin strokes and ring strength. |
| 026 | [Médaille pour animal](https://to7fa.ma/produits/medaille-pour-animal) | To7fa | dès 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=personalized%20pet%20tag) · [Printables](https://www.printables.com/search/models?q=personalized%20pet%20tag) | Use a flat-backed version; check thin strokes and ring strength. |
| 027 | [Porte-crayons Trio Prénom](https://to7fa.ma/produits/porte-crayons-trio-prenom) | To7fa | 85 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=personalized%20pencil%20holder) · [Printables](https://www.printables.com/search/models?q=personalized%20pencil%20holder) | Geometry, dimensions and supports unknown until file inspection. |
| 028 | [Support téléphone galbé](https://to7fa.ma/produits/support-telephone-galbe) | To7fa | 65 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=curved%20phone%20stand) · [Printables](https://www.printables.com/search/models?q=curved%20phone%20stand) | Check orientation, bridges, fit and load; no-support printing unverified. |
| 029 | [Initiales de couple personnalisées](https://to7fa.ma/produits/initiales-de-couple-personnalisees) | To7fa | 149 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=couple%20initials%20sculpture) · [Printables](https://www.printables.com/search/models?q=couple%20initials%20sculpture) | Geometry, dimensions and supports unknown until file inspection. |
| 030 | [Étui à Briquet Écailles](https://to7fa.ma/produits/etui-a-briquet-ecailles) | To7fa | 39 MAD | HOLD | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=scales%20lighter%20case) · [Printables](https://www.printables.com/search/models?q=scales%20lighter%20case) | Fit and heat exposure require evaluation; not an initial PLA product. |
| 031 | [Étui Briquet Alvéolé](https://to7fa.ma/produits/etui-briquet-alveole) | To7fa | 39 MAD | HOLD | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=honeycomb%20lighter%20sleeve) · [Printables](https://www.printables.com/search/models?q=honeycomb%20lighter%20sleeve) | Fit and heat exposure require evaluation; not an initial PLA product. |
| 032 | [Boucles d'Oreilles Initiale Personnalisée](https://to7fa.ma/produits/boucles-d-oreilles-initiale-personnalisee) | To7fa | dès 19 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=initial%20earrings) · [Printables](https://www.printables.com/search/models?q=initial%20earrings) | Fine details and attachment holes need a test; add suitable earring hardware. |
| 033 | [Boucles Mandala Azur](https://to7fa.ma/produits/boucles-mandala-azur) | To7fa | dès 19 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=mandala%20earrings) · [Printables](https://www.printables.com/search/models?q=mandala%20earrings) | Fine details and attachment holes need a test; add suitable earring hardware. |
| 034 | [Boucles Pâquerette Tressée](https://to7fa.ma/produits/boucles-paquerette-tressee) | To7fa | dès 19 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=daisy%20earrings) · [Printables](https://www.printables.com/search/models?q=daisy%20earrings) | Fine details and attachment holes need a test; add suitable earring hardware. |
| 035 | [Porte-bougies et décoration Happy Birthday](https://to7fa.ma/produits/boite-cadeau-happy-birthday) | To7fa | 55 MAD | HOLD | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=happy%20birthday%20decoration) · [Printables](https://www.printables.com/search/models?q=happy%20birthday%20decoration) | Do not expose PLA to embers or flame; redesign as decorative-only or assess a heat-resistant insert. |
| 036 | [Support téléphone essentiel](https://to7fa.ma/produits/support-telephone-essentiel) | To7fa | 59 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=simple%20phone%20stand) · [Printables](https://www.printables.com/search/models?q=simple%20phone%20stand) | Check orientation, bridges, fit and load; no-support printing unverified. |
| 037 | [Fourreau Porte-Clés pour Briquet](https://to7fa.ma/produits/fourreau-porte-cles-pour-briquet) | To7fa | 35 MAD | HOLD | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=lighter%20keychain%20sleeve) · [Printables](https://www.printables.com/search/models?q=lighter%20keychain%20sleeve) | Fit and heat exposure require evaluation; not an initial PLA product. |
| 038 | [Étui Nomade pour Mini Briquet](https://to7fa.ma/produits/etui-nomade-pour-mini-briquet) | To7fa | 35 MAD | HOLD | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=mini%20lighter%20case) · [Printables](https://www.printables.com/search/models?q=mini%20lighter%20case) | Fit and heat exposure require evaluation; not an initial PLA product. |
| 039 | [Boucles d'Oreilles Colibri Aérien](https://to7fa.ma/produits/boucles-d-oreilles-colibri-aerien) | To7fa | dès 19 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=hummingbird%20earrings) · [Printables](https://www.printables.com/search/models?q=hummingbird%20earrings) | Fine details and attachment holes need a test; add suitable earring hardware. |
| 040 | [Boucles d'Oreilles Coquillage](https://to7fa.ma/produits/boucles-d-oreilles-coquillage) | To7fa | dès 19 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=shell%20earrings) · [Printables](https://www.printables.com/search/models?q=shell%20earrings) | Fine details and attachment holes need a test; add suitable earring hardware. |
| 041 | [Boucles d'Oreilles Dentelle Blanche](https://to7fa.ma/produits/boucles-d-oreilles-dentelle-blanche) | To7fa | dès 19 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=lace%20earrings) · [Printables](https://www.printables.com/search/models?q=lace%20earrings) | Fine details and attachment holes need a test; add suitable earring hardware. |
| 042 | [Boucles d'Oreilles Rose Délicate](https://to7fa.ma/produits/boucles-d-oreilles-rose-delicate) | To7fa | dès 19 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=rose%20earrings) · [Printables](https://www.printables.com/search/models?q=rose%20earrings) | Fine details and attachment holes need a test; add suitable earring hardware. |
| 043 | [Porte-Encens Cascade Céleste](https://to7fa.ma/produits/porte-encens-cascade-celeste) | To7fa | 89 MAD | HOLD | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=waterfall%20incense%20holder) · [Printables](https://www.printables.com/search/models?q=waterfall%20incense%20holder) | Do not expose PLA to embers or flame; redesign as decorative-only or assess a heat-resistant insert. |
| 044 | [Écrin Porte-Encens Zen](https://to7fa.ma/produits/ecrin-porte-encens-zen) | To7fa | 89 MAD | HOLD | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=zen%20incense%20holder) · [Printables](https://www.printables.com/search/models?q=zen%20incense%20holder) | Do not expose PLA to embers or flame; redesign as decorative-only or assess a heat-resistant insert. |
| 045 | [Boucles d'Oreilles Douces Pattes](https://to7fa.ma/produits/boucles-d-oreilles-douces-pattes) | To7fa | dès 19 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=paw%20earrings) · [Printables](https://www.printables.com/search/models?q=paw%20earrings) | Fine details and attachment holes need a test; add suitable earring hardware. |
| 046 | [Patère Murale Épure](https://to7fa.ma/produits/patere-murale-epure) | To7fa | 35 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=minimal%20wall%20hook) · [Printables](https://www.printables.com/search/models?q=minimal%20wall%20hook) | Check orientation, bridges, fit and load; no-support printing unverified. |
| 047 | [Mini support de poche](https://to7fa.ma/produits/mini-support-de-poche) | To7fa | 35 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=pocket%20phone%20stand) · [Printables](https://www.printables.com/search/models?q=pocket%20phone%20stand) | Check orientation, bridges, fit and load; no-support printing unverified. |
| 048 | [Support téléphone bicolore](https://to7fa.ma/produits/support-telephone-bicolore) | To7fa | 55 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=two%20part%20phone%20stand) · [Printables](https://www.printables.com/search/models?q=two%20part%20phone%20stand) | Check orientation, bridges, fit and load; no-support printing unverified. |
| 049 | [Monogramme prénom](https://to7fa.ma/produits/monogramme-prenom) | To7fa | 119 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=personalized%20monogram) · [Printables](https://www.printables.com/search/models?q=personalized%20monogram) | Use a flat-backed version; check thin strokes and ring strength. |
| 050 | [Vase Japandi Shizu](https://to7fa.ma/produits/vase-japandi-shizu) | To7fa | 129 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=japandi%20vase) · [Printables](https://www.printables.com/search/models?q=japandi%20vase) | Check overhangs; use a liner for water; dimensions unverified. |
| 051 | [Range-câbles USB](https://to7fa.ma/produits/range-cables-usb) | To7fa | 39 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=USB%20cable%20organizer) · [Printables](https://www.printables.com/search/models?q=USB%20cable%20organizer) | Geometry, dimensions and supports unknown until file inspection. |
| 052 | [Pot à crayons côtelé](https://to7fa.ma/produits/pot-a-crayons-cotele) | To7fa | 85 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=ribbed%20pencil%20cup) · [Printables](https://www.printables.com/search/models?q=ribbed%20pencil%20cup) | Geometry, dimensions and supports unknown until file inspection. |
| 053 | [Coussin pour téléphone](https://to7fa.ma/produits/coussin-pour-telephone) | To7fa | 149 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=cushion%20phone%20stand) · [Printables](https://www.printables.com/search/models?q=cushion%20phone%20stand) | Check orientation, bridges, fit and load; no-support printing unverified. |
| 054 | [Crochet à casque](https://to7fa.ma/produits/crochet-a-casque) | To7fa | 49 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=headphone%20hook) · [Printables](https://www.printables.com/search/models?q=headphone%20hook) | Check orientation, bridges, fit and load; no-support printing unverified. |
| 055 | [Cache-pot sur pieds](https://to7fa.ma/produits/cache-pot-sur-pieds) | To7fa | 219 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=planter%20separate%20legs) · [Printables](https://www.printables.com/search/models?q=planter%20separate%20legs) | Check overhangs; use a liner for water; dimensions unverified. |
| 056 | [Porte-clés lettre d'amour](https://to7fa.ma/produits/porte-cles-lettre-d-amour) | To7fa | 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=love%20letter%20keychain) · [Printables](https://www.printables.com/search/models?q=love%20letter%20keychain) | Use a flat-backed version; check thin strokes and ring strength. |
| 057 | [Lampe Champignon Côtelée](https://to7fa.ma/produits/lampe-champignon-cotelee) | To7fa | 279 MAD | HOLD | Blue or white | Separate parts; 0 per monochrome batch | [MakerWorld](https://makerworld.com/en/search/models?keyword=ribbed%20mushroom%20lamp) · [Printables](https://www.printables.com/search/models?q=ribbed%20mushroom%20lamp) | Additional LED hardware, assembly and temperature evaluation. |
| 058 | [Vase Vanta](https://to7fa.ma/produits/vase-vanta) | To7fa | 99 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=modern%20vase) · [Printables](https://www.printables.com/search/models?q=modern%20vase) | Check overhangs; use a liner for water; dimensions unverified. |
| 059 | [Marque-page Japon](https://to7fa.ma/produits/marque-page-japon) | To7fa | 35 MAD | FIRST | Blue + white | Raised face by layer; 1 planned change | [MakerWorld](https://makerworld.com/en/search/models?keyword=Japanese%20bookmark) · [Printables](https://www.printables.com/search/models?q=Japanese%20bookmark) | Use a flat-backed version; check thin strokes and ring strength. |
| 060 | [Vase Soliflore Facetté](https://to7fa.ma/produits/vase-soliflore-facette) | To7fa | 69 MAD | TEST | Blue or white | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=faceted%20bud%20vase) · [Printables](https://www.printables.com/search/models?q=faceted%20bud%20vase) | Check overhangs; use a liner for water; dimensions unverified. |
| 061 | [Fantasia horsemen relief](https://3dgifi.ma/product/fantasia-horsemen-relief-sculpture/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=fantasia%20horsemen%20relief) · [Printables](https://www.printables.com/search/models?q=fantasia%20horsemen%20relief) | Complex geometry: support-free printing and dimensions unverified. |
| 062 | [Airplane models](https://3dgifi.ma/product/3d-airplane-models/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=airplane%20model%20split%20parts) · [Printables](https://www.printables.com/search/models?q=airplane%20model%20split%20parts) | Complex geometry: support-free printing and dimensions unverified. |
| 063 | [Articulated Christmas pack](https://3dgifi.ma/product/christmas-packs/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=articulated%20christmas%20ornaments) · [Printables](https://www.printables.com/search/models?q=articulated%20christmas%20ornaments) | Complex geometry: support-free printing and dimensions unverified. |
| 064 | [Articulated Christmas tree](https://3dgifi.ma/product/3d-articulated-christmas-tree/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=articulated%20christmas%20tree) · [Printables](https://www.printables.com/search/models?q=articulated%20christmas%20tree) | Complex geometry: support-free printing and dimensions unverified. |
| 065 | [Minecraft heroes](https://3dgifi.ma/product/3d-articulated-minecraft-heroes/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=original%20articulated%20block%20character) · [Printables](https://www.printables.com/search/models?q=original%20articulated%20block%20character) | Branded/character reference: do not assume commercial rights. Search term intentionally targets an original alternative. |
| 066 | [Christmas wall and door decorations](https://3dgifi.ma/product/3d-christmas-decor/) | 3DGIFI | Not transcribed; check product page | TEST | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=christmas%20corner%20decoration) · [Printables](https://www.printables.com/search/models?q=christmas%20corner%20decoration) | Complex geometry: support-free printing and dimensions unverified. |
| 067 | [Mohammed V mausoleum](https://3dgifi.ma/product/mausoleum-of-mohammed-v/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=Mohammed%20V%20mausoleum%20miniature) · [Printables](https://www.printables.com/search/models?q=Mohammed%20V%20mausoleum%20miniature) | Complex geometry: support-free printing and dimensions unverified. |
| 068 | [Andalusian music diva statue](https://3dgifi.ma/product/3d-statue-diva-of-moroccan-andalusian-music/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=Moroccan%20musician%20statue) · [Printables](https://www.printables.com/search/models?q=Moroccan%20musician%20statue) | Complex geometry: support-free printing and dimensions unverified. |
| 069 | [Photo relief with thuya wood](https://3dgifi.ma/product/3d-wood-relief-photo/) | 3DGIFI | Not transcribed; check product page | TEST | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=photo%20relief%20frame) · [Printables](https://www.printables.com/search/models?q=photo%20relief%20frame) | Wood component is not printable PLA; redesign frame and inspect relief geometry. |
| 070 | [Snail lamp](https://3dgifi.ma/product/snail-lamp/) | 3DGIFI | Not transcribed; check product page | HOLD | Black + white; red or blue accents | Separate parts; 0 per monochrome batch | [MakerWorld](https://makerworld.com/en/search/models?keyword=snail%20LED%20lamp) · [Printables](https://www.printables.com/search/models?q=snail%20LED%20lamp) | Assembly required; check component dimensions, fits and extra hardware. Assess LED heat and ventilation. |
| 071 | [Gnawa Kbakab statue](https://3dgifi.ma/product/statue-gnawa-kbakab/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=Gnawa%20musician%20statue) · [Printables](https://www.printables.com/search/models?q=Gnawa%20musician%20statue) | Complex geometry: support-free printing and dimensions unverified. |
| 072 | [Mushroom lamp](https://3dgifi.ma/product/3d-printed-mushroom-lamp/) | 3DGIFI | Not transcribed; check product page | HOLD | Black + white; red or blue accents | Separate parts; 0 per monochrome batch | [MakerWorld](https://makerworld.com/en/search/models?keyword=mushroom%20lamp%20separate%20parts) · [Printables](https://www.printables.com/search/models?q=mushroom%20lamp%20separate%20parts) | Assembly required; check component dimensions, fits and extra hardware. Assess LED heat and ventilation. |
| 073 | [Hassan II mosque](https://3dgifi.ma/product/hassan-ii-mosque/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=Hassan%20II%20mosque%20miniature) · [Printables](https://www.printables.com/search/models?q=Hassan%20II%20mosque%20miniature) | Complex geometry: support-free printing and dimensions unverified. |
| 074 | [Hassan Tower](https://3dgifi.ma/product/hassan-tower/) | 3DGIFI | Not transcribed; check product page | TEST | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=Hassan%20tower%20miniature) · [Printables](https://www.printables.com/search/models?q=Hassan%20tower%20miniature) | Complex geometry: support-free printing and dimensions unverified. |
| 075 | [Heart vases](https://3dgifi.ma/product/hearts-vases/) | 3DGIFI | Not transcribed; check product page | TEST | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=heart%20vase) · [Printables](https://www.printables.com/search/models?q=heart%20vase) | Complex geometry: support-free printing and dimensions unverified. Use a water liner; inspect overhangs. |
| 076 | [Hello Kitty lamp](https://3dgifi.ma/product/hello-kitty-3d-lamp/) | 3DGIFI | Not transcribed; check product page | HOLD | Black + white; red or blue accents | Separate parts; 0 per monochrome batch | [MakerWorld](https://makerworld.com/en/search/models?keyword=original%20cat%20LED%20lamp) · [Printables](https://www.printables.com/search/models?q=original%20cat%20LED%20lamp) | Branded/character reference: do not assume commercial rights. Search term intentionally targets an original alternative. |
| 077 | [Homer can holder](https://3dgifi.ma/product/homer-can-holder/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=generic%20face%20can%20holder) · [Printables](https://www.printables.com/search/models?q=generic%20face%20can%20holder) | Branded/character reference: do not assume commercial rights. Search term intentionally targets an original alternative. |
| 078 | [Koutoubia mosque](https://3dgifi.ma/product/kutubiyya-mosque/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=Koutoubia%20mosque%20miniature) · [Printables](https://www.printables.com/search/models?q=Koutoubia%20mosque%20miniature) | Complex geometry: support-free printing and dimensions unverified. |
| 079 | [Laayoune gate](https://3dgifi.ma/product/laayoune-gate/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=Laayoune%20gate%20miniature) · [Printables](https://www.printables.com/search/models?q=Laayoune%20gate%20miniature) | Complex geometry: support-free printing and dimensions unverified. |
| 080 | [Labubu figurine](https://3dgifi.ma/product/labubu-3d-figurine/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=original%20creature%20figurine) · [Printables](https://www.printables.com/search/models?q=original%20creature%20figurine) | Branded/character reference: do not assume commercial rights. Search term intentionally targets an original alternative. |
| 081 | [Lattice planter](https://3dgifi.ma/product/lattice-planter/) | 3DGIFI | Not transcribed; check product page | TEST | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=lattice%20planter) · [Printables](https://www.printables.com/search/models?q=lattice%20planter) | Complex geometry: support-free printing and dimensions unverified. Use a water liner; inspect overhangs. |
| 082 | [Houssine Toulali statue](https://3dgifi.ma/product/statue-malhoun-exquise-houssine-toulali/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=Moroccan%20singer%20statue) · [Printables](https://www.printables.com/search/models?q=Moroccan%20singer%20statue) | Complex geometry: support-free printing and dimensions unverified. |
| 083 | [Selham statue, advertised 45 cm](https://3dgifi.ma/product/3d-printed-selham-statue/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=Moroccan%20selham%20statue) · [Printables](https://www.printables.com/search/models?q=Moroccan%20selham%20statue) | Advertised 450 mm height exceeds A1 in one piece: split or redesign; verify all dimensions. |
| 084 | [LOGOWATCH logo clock](https://3dgifi.ma/product/logowatch/) | 3DGIFI | Not transcribed; check product page | HOLD | Black + white; red or blue accents | Separate parts; 0 per monochrome batch | [MakerWorld](https://makerworld.com/en/search/models?keyword=custom%20logo%20wall%20clock) · [Printables](https://www.printables.com/search/models?q=custom%20logo%20wall%20clock) | Assembly required; check component dimensions, fits and extra hardware. |
| 085 | [Mario planter](https://3dgifi.ma/product/mario-planter/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=original%20geometric%20planter) · [Printables](https://www.printables.com/search/models?q=original%20geometric%20planter) | Branded/character reference: do not assume commercial rights. Search term intentionally targets an original alternative. Use a water liner; inspect overhangs. |
| 086 | [Bab El Mansour](https://3dgifi.ma/product/bab-el-mansour/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=Bab%20Mansour%20miniature) · [Printables](https://www.printables.com/search/models?q=Bab%20Mansour%20miniature) | Complex geometry: support-free printing and dimensions unverified. |
| 087 | [MEMOMAP personalised map](https://3dgifi.ma/product/memomap/) | 3DGIFI | Not transcribed; check product page | TEST | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=city%20map%20relief) · [Printables](https://www.printables.com/search/models?q=city%20map%20relief) | Complex geometry: support-free printing and dimensions unverified. |
| 088 | [Menara Gardens](https://3dgifi.ma/product/menara-gardens/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=Menara%20gardens%20miniature) · [Printables](https://www.printables.com/search/models?q=Menara%20gardens%20miniature) | Complex geometry: support-free printing and dimensions unverified. |
| 089 | [MINIU personalised figurine](https://3dgifi.ma/product/miniu-figurines/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=custom%20portrait%20figurine) · [Printables](https://www.printables.com/search/models?q=custom%20portrait%20figurine) | Complex geometry: support-free printing and dimensions unverified. |
| 090 | [MINIU miniature universe](https://3dgifi.ma/product/miniu-your-mini-universe-in-3d/) | 3DGIFI | Not transcribed; check product page | HOLD | Black + white; red or blue accents | Separate parts; 0 per monochrome batch | [MakerWorld](https://makerworld.com/en/search/models?keyword=custom%20miniature%20diorama) · [Printables](https://www.printables.com/search/models?q=custom%20miniature%20diorama) | Assembly required; check component dimensions, fits and extra hardware. |
| 091 | [Moon lamp](https://3dgifi.ma/product/3d-printed-moon-lamp/) | 3DGIFI | Not transcribed; check product page | HOLD | Black + white; red or blue accents | Separate parts; 0 per monochrome batch | [MakerWorld](https://makerworld.com/en/search/models?keyword=moon%20LED%20lamp) · [Printables](https://www.printables.com/search/models?q=moon%20LED%20lamp) | Assembly required; check component dimensions, fits and extra hardware. Assess LED heat and ventilation. |
| 092 | [Moroccan football dama, 50 × 50 cm](https://3dgifi.ma/product/moroccan-football-dama/) | 3DGIFI | Not transcribed; check product page | HOLD | Black + white; red or blue accents | Separate parts; 0 per monochrome batch | [MakerWorld](https://makerworld.com/en/search/models?keyword=modular%20checkers%20board) · [Printables](https://www.printables.com/search/models?q=modular%20checkers%20board) | Advertised 500 × 500 mm board exceeds A1 in one piece: modular redesign required. |
| 093 | [Moroccan football heroes](https://3dgifi.ma/product/moroccan-football-heroes-figurines/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=original%20football%20player%20figurine) · [Printables](https://www.printables.com/search/models?q=original%20football%20player%20figurine) | Complex geometry: support-free printing and dimensions unverified. |
| 094 | [Moroccan horse bust](https://3dgifi.ma/product/moroccan-horse-bust/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=horse%20bust) · [Printables](https://www.printables.com/search/models?q=horse%20bust) | Complex geometry: support-free printing and dimensions unverified. |
| 095 | [MRMDEN Ramadan figurine](https://3dgifi.ma/product/mrmden/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=original%20Ramadan%20figurine) · [Printables](https://www.printables.com/search/models?q=original%20Ramadan%20figurine) | Complex geometry: support-free printing and dimensions unverified. |
| 096 | [Crow lamp](https://3dgifi.ma/product/mysterious-crow-lamp/) | 3DGIFI | Not transcribed; check product page | HOLD | Black + white; red or blue accents | Separate parts; 0 per monochrome batch | [MakerWorld](https://makerworld.com/en/search/models?keyword=crow%20LED%20lamp) · [Printables](https://www.printables.com/search/models?q=crow%20LED%20lamp) | Assembly required; check component dimensions, fits and extra hardware. Assess LED heat and ventilation. |
| 097 | [Together vase](https://3dgifi.ma/product/together-vase-2/) | 3DGIFI | Not transcribed; check product page | TEST | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=raindrop%20lattice%20vase) · [Printables](https://www.printables.com/search/models?q=raindrop%20lattice%20vase) | Complex geometry: support-free printing and dimensions unverified. Use a water liner; inspect overhangs. |
| 098 | [Travel chess board](https://3dgifi.ma/product/travel-chess-board/) | 3DGIFI | Not transcribed; check product page | HOLD | Black + white; red or blue accents | Separate parts; 0 per monochrome batch | [MakerWorld](https://makerworld.com/en/search/models?keyword=travel%20chess%20board) · [Printables](https://www.printables.com/search/models?q=travel%20chess%20board) | Assembly required; check component dimensions, fits and extra hardware. |
| 099 | [Personalised gamer bust stand](https://3dgifi.ma/product/3d-gamer-bust/) | 3DGIFI | Not transcribed; check product page | HOLD | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=headphone%20stand%20bust) · [Printables](https://www.printables.com/search/models?q=headphone%20stand%20bust) | Complex geometry: support-free printing and dimensions unverified. |
| 100 | [Photo relief in Moroccan frame](https://3dgifi.ma/product/3d-relief-artwork/) | 3DGIFI | Not transcribed; check product page | TEST | White or black | Single colour; 0 planned changes | [MakerWorld](https://makerworld.com/en/search/models?keyword=photo%20relief%20Moroccan%20frame) · [Printables](https://www.printables.com/search/models?q=photo%20relief%20Moroccan%20frame) | Complex geometry: support-free printing and dimensions unverified. |

## Five concrete model-file leads

These specific pages appeared in search results. Direct page retrieval failed, so author/licence and printability are not verified. They are starting leads, not approved files for sale.

| Model lead | Author shown in search | Use | Licence |
|---|---|---|---|
| [Customizable Keychain with Name](https://www.printables.com/model/805674-customizable-keychain-with-name) | Apolleon | Name-keychain starting point; indexed description mentions a Fusion 360 file | Unknown |
| [Car licence plate keychain V2](https://www.printables.com/model/873692-car-license-plate-keychain-v2) | michele MM3D | Plate-keychain starting point; adapt layout only if permitted | Unknown |
| [Shirt keychain](https://www.printables.com/model/613397-shirt-keychain) | 3D Print A Lot | Shirt/name/number concept | Unknown |
| [QR code display stand](https://cults3d.com/en/3d-model/art/qr-code-display-stand) | Unknown | QR stand candidate | Unknown |
| [QR code stand](https://cults3d.com/en/3d-model/gadget/qr-code-stand) | Unknown | Alternative QR stand candidate | Unknown |

## Websites for finding printable files

| Website | How to use it |
|---|---|
| [SliSearch](https://slisearch.com/en) | Paste a row's query; follow the result to the original creator. An index is not a licence authority. |
| [MakerWorld](https://makerworld.com/en) | Find STL/3MF and print profiles; inspect profile printer settings. Check the model-specific licence or creator's commercial membership. |
| [Printables](https://www.printables.com) | Search STL and parametric designs; inspect files, makes and licence. |
| [Cults3D](https://cults3d.com) | Search free/paid models; purchase of a file alone does not establish commercial printing permission. |
| [Thangs](https://thangs.com) | Search designers and models; inspect any commercial membership's covered models and conditions. |

Search terms are embedded in every model-search link. Use generic terms rather than a shop's proprietary product name when seeking independent alternatives.

## Recommended first prototype batch

Begin with references 001, 002, 003, 004, 007, 011, 012, 016, 023 and 026: name keychains, plates, party tags, initials and pet tags. These share a flat base and raised-text design approach. Print one sample of each exact file before advertising it.

Two useful additions outside the 100-row count:
- QR stands: the To7fa catalogue lists an NFC/QR review display. Use a white field and black modules, preserve the QR quiet zone, and test scanning with several phones before selling. NFC requires a separate tag.
- Pixel-art kits: [3DGIFI home](https://3dgifi.ma/) lists a Pixel Emoji 24 × 24 kit. Search “pixel art tile grid” or “pixel mosaic kit”; print black, white, blue and red tiles separately. Check tile-to-grid fit before a full batch. Do not copy their exact artwork unless permitted.

## Evidence log and limitations

To7fa source: https://to7fa.ma/produits — catalogue read and product URLs extracted; prices are observations, not quotations guaranteed at checkout. “Dès” means “from”. No individual To7fa product audit was performed for this report.

3DGIFI catalogue sources: https://3dgifi.ma/shop/ ; https://3dgifi.ma/shop/page/4/ ; https://3dgifi.ma/shop/page/5/ ; https://3dgifi.ma/shop/page/6/ . Pages 2 and 3 were unavailable or inconsistent, so no claim is made that these are the first 40 in current sort order. Product-page retrieval results are recorded below. Cached pages do not verify stock today.

Technical reference: https://bambulab.cn/zh-cn/a1/tech-specs (official indexed technical specifications). Commercial-membership reference: https://blog.bambulab.com/empowering-our-creators-with-new-commercial-license-membership/ . Search-index description: https://slisearch.com/en/docs .

| Reference | Evidence status | Exact file / licence / sliced validation |
|---|---|---|
| 001 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 002 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 003 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 004 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 005 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 006 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 007 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 008 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 009 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 010 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 011 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 012 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 013 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 014 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 015 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 016 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 017 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 018 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 019 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 020 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 021 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 022 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 023 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 024 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 025 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 026 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 027 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 028 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 029 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 030 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 031 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 032 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 033 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 034 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 035 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 036 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 037 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 038 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 039 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 040 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 041 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 042 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 043 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 044 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 045 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 046 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 047 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 048 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 049 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 050 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 051 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 052 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 053 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 054 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 055 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 056 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 057 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 058 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 059 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 060 | Catalogue listing read; individual page not audited | Unknown / unknown / not performed |
| 061 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 062 | Catalogue listing only; product page retrieval failed | Unknown / unknown / not performed |
| 063 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 064 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 065 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 066 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 067 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 068 | Catalogue listing only; product page retrieval failed | Unknown / unknown / not performed |
| 069 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 070 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 071 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 072 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 073 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 074 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 075 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 076 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 077 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 078 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 079 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 080 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 081 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 082 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 083 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 084 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 085 | Catalogue listing only; product page retrieval failed | Unknown / unknown / not performed |
| 086 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 087 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 088 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 089 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 090 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 091 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 092 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 093 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 094 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 095 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 096 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 097 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 098 | Catalogue listing only; product page retrieval failed | Unknown / unknown / not performed |
| 099 | Product page retrieved; may be cached | Unknown / unknown / not performed |
| 100 | Product page retrieved; may be cached | Unknown / unknown / not performed |
```

## Fichier prompts/README.md

````markdown
# Démarrer MustDesign3D

## Reprise Gemini et Copilot

Le [paquet de reprise](handoff/README.md) fournit les deux versions du prompt maître, un plan pour chaque environnement et un brief de génération photo. Le fichier PROJECT_SOURCE.md est régénéré depuis le code avec `npm run handoff`. Le README reçu en pièce jointe est resté en lecture seule.

Le nouveau catalogue de démonstration contient neuf références et trois collections. Les études historiques restent dans la galerie technique. Consulter le README du projet pour l’état actuel du code avant de reprendre un ancien jalon ci-dessous.

Mise à jour du 10 novembre 2026. Ce dossier contient les prompts pour développer la prochaine version de MustDesign3D et le relevé des sources demandé. Le site actuel est une démo locale existante.

## 1. Comprendre les livrables

- [Prompt maître](00-master-mustdesign3d.md) fixe la marque, le périmètre et les règles communes.
- [Recherche et sélection](recherche/01-sources-et-selection.md) compare les trois références et propose dix concepts à étudier.
- [Inventaire To7fa](recherche/02-inventaire-to7fa.md) contient les 227 adresses produit relevées dans le sitemap public.
- [Bibliothèque des modèles](recherche/03-modeles-et-import.md) décrit les candidats SliSearch, leur niveau de vérification et le processus d’acquisition.
- Les trois prompts frontend et les trois prompts backend détaillent les prochains changements du code.

Le relevé est un inventaire de liens. Les fichiers STL, 3MF, SCAD et les images doivent être acquis séparément depuis leurs sources avec les droits correspondants.

## 2. Préparer le poste local

1. Ouvrir le projet dans VS Code.
2. Vérifier les instructions AGENTS.md applicables et lire codex.md, puis 00-master-mustdesign3d.md.
3. Vérifier Node et npm dans PowerShell.

```powershell
Set-Location 'C:\Users\mekka\Desktop\codex\3d-printing-website'
node --version
npm.cmd --version
```

Le package.json demande Node 22.x. Utiliser cette version pour aligner le développement et la future exécution Railway. Le poste avait Node 25 lors de la création de la démo.

4. Installer les versions verrouillées.

```powershell
npm.cmd ci
```

5. Vérifier si un serveur utilise déjà le port de la démo.

```powershell
Get-NetTCPConnection -LocalPort 3137 -State Listen -ErrorAction SilentlyContinue
```

Si la démo répond déjà, l’ouvrir sur http://localhost:3137. Pour lancer une session de développement distincte, utiliser un autre port.

```powershell
npm.cmd run dev -- --port 3138
```

Ouvrir http://localhost:3138. Conserver la fenêtre du terminal ouverte. Ctrl+C arrête cette session.

## 3. Commencer par la recherche

1. Lire les trois pages de référence avec Search Service, puis consulter les sources d’origine des modèles retenus.
2. Utiliser l’inventaire To7fa pour comparer les familles de produits. Choisir dix concepts puis trois priorités parmi le porte-clés, la plaque de bureau et le support QR.
3. Pour SliSearch, rechercher un besoin précis avec le filtre commercial et vérifier ensuite la licence chez le créateur. Utiliser les requêtes du document modèles.
4. Enregistrer auteur, adresse d’origine, date de contrôle et droits dans le registre interne. Garder un statut inconnu tant que la source primaire manque.
5. Évaluer chaque concept pour l’A1, puis trancher dans Bambu Studio après acquisition d’un fichier autorisé.
6. Préparer des textes et des visuels MustDesign3D originaux. Photographier les premiers prototypes.

Les prix concurrents constituent des observations datées. Les prix de vente MustDesign3D nécessitent un calcul de fabrication et de livraison.

## 4. Développer dans cet ordre

| Étape | Prompt | Résultat vérifiable |
| --- | --- | --- |
| 1 | [Backend 01](backend/01-contrats-et-donnees.md) | Contrats partagés, identifiants stables et séparation catalogue/recherche |
| 2 | [Frontend 01](frontend/01-fondations-et-accueil.md) | Accueil MustDesign3D, contact et navigation mobile |
| 3 | [Frontend 02](frontend/02-catalogue-et-personnalisation.md) | Catalogue, fiches et options personnalisables |
| 4 | [Frontend 03](frontend/03-panier-et-parcours-client.md) | Panier persistant localement et parcours démo |
| 5 | [Backend 02](backend/02-commandes-et-devis.md) | Lecture API et verrou serveur des écritures démo |
| 6 | [Backend 03, recette locale](backend/03-railway-et-recette.md) | Build et parcours vérifiés localement |
| Après validation | Backend 01 puis 02, jalon commandes | PostgreSQL local, migrations et commandes avec données de test |
| Après demande explicite | Backend 03, publication | Déploiement Railway et contrôle de l’usage |

Exécuter un prompt à la fois. Après chaque étape, demander un résumé des fichiers modifiés, des tests exécutés et des limites restantes. Conserver codex.md et les URLs produit existantes.

## 5. Employer les skills et outils adaptés

| Besoin | Skill ou outil | Usage |
| --- | --- | --- |
| Trouver des produits et vérifier les références | Search Service | Liens publics, faits datés, sources primaires, journal des échecs |
| Revoir les contrats et migrations PostgreSQL | postgresql-code-review | Contraintes, clés étrangères, transactions, JSONB et accès serveur |
| Réviser le moteur PostgreSQL lors du jalon commandes | postgresql-optimization, si disponible | Requêtes mesurées et index associés aux accès réels |
| Préparer un nouveau projet TypeScript isolé | typescript-setup, si disponible | Réserver à un nouveau projet ou à une configuration manquante |
| Tester le site | Navigateur ou Playwright disponible | Mobile, clavier, RTL, personnalisation et panier |

Le skill postgresql-code-review a été lu pendant la préparation de ces prompts. Les autres sont des choix pour leurs étapes respectives. Avant d’en utiliser un, le retrouver dans le catalogue actif et lire son SKILL.md. Si le skill manque, poursuivre avec la documentation officielle et signaler ce remplacement.

Les anciens skills d’artefacts proposent un bundling HTML autonome. La cible de ce projet reste Next.js. Leurs règles de lisibilité et de composition peuvent guider les visuels lorsqu’ils sont disponibles.

## 6. Vérifier avant de demander la publication

```powershell
npm.cmd run typecheck
npm.cmd run build
```

- Accueil, boutique, contact et six fiches existantes accessibles.
- Recherche, catégories et état vide cohérents.
- Prénom français, arabe et bilingue conservés jusqu’au panier.
- Prix indicatifs calculés en centimes de MAD.
- À 320, 390 et 1440 px, contenu lisible et sans débordement horizontal.
- Navigation clavier, fermeture du panier avec Échap et retour du focus fonctionnels.
- Chaque ajout au catalogue possède une provenance et un statut de vérification.
- Démo publique ou locale démo sans saisie de coordonnées ni écriture de commande.

## 7. État de cette mise à jour documentaire

Le jalon démo des six prompts est maintenant implémenté localement : contrats partagés, six produits/prix conservés, visuels originaux, personnalisation par produit, panier structuré/persistant/éditable, pages projet/professionnels/récapitulatif et API catalogue avec verrou des écritures. Six sources OpenSCAD originales privées et leur manifeste sont fournis, sans acquisition de modèle concurrent ni validation de fabrication revendiquée.

Le [README du projet](../README.md) détaille le démarrage, la configuration et les limites réelles. PostgreSQL, migrations, traitement des commandes/devis réels, acquisition de modèles tiers et publication Railway restent des jalons ultérieurs. Aucun service cloud n’a été utilisé pour cette itération.

La reprise suivante ajoute une septième création originale, la plaque pixel Zellige, une galerie /modeles et des vues générées par OpenSCAD pour les sept prototypes. Les exports STL sont disponibles dans production/exports/. Le prix de 119 MAD de la plaque est une hypothèse de démo. La [note de sélection et d’intégration](recherche/04-selection-et-integration.md) contient les résultats Search Service et la procédure d’ajout d’un prochain modèle.
````

## Fichier prompts/backend/01-contrats-et-donnees.md

```markdown
# Backend 01 — Contrats et données MustDesign3D

## Mission et périmètre du jalon

Lis prompts/00-master-mustdesign3d.md, les documents de recherche, lib/products.ts et app/cart.tsx. Définis les contrats TypeScript communs au catalogue, à la personnalisation, au panier, aux modèles et aux commandes.

Le premier livrable utilise les données locales. PostgreSQL et les migrations constituent le jalon commandes, à développer localement après validation de la démo.

## 1. Compatibilité avec la démo

Le Product actuel possède slug, name, category, price, description et mark. price représente déjà des centimes de MAD. Les six slugs sont des URLs établies.

Ajouter un id explicite stable aux six entrées. Migrer price vers priceCents en une modification cohérente de tous les consommateurs, y compris formatPrice, cartes, fiches, panier et configurateur. Garder une seule valeur autoritaire du prix. Le champ mark sert de texte de repli des visuels actuels.

| Slug conservé | Identifiant stable |
| --- | --- |
| porte-cles-prenom | md-keychain-01 |
| plaque-bureau | md-desk-01 |
| ville-maroc | md-city-01 |
| support-qr | md-qr-01 |
| logo-bureau | md-logo-01 |
| plaque-porte | md-door-01 |

Le panier est actuellement en mémoire, avec une clé calculée depuis les options et details en texte. Le nouveau CartLine contient les options structurées. Lors de l’ajout de la persistance, utiliser schemaVersion=1 et vérifier chaque ligne à la restauration.

## 2. Contrats publics

Définir les types ci-dessous et leurs validations partagées.

| Type | Contenu minimum |
| --- | --- |
| Product | id, slug, name, shortDescription, description, categoryId, priceCents, currency='MAD', images, mark, featured, status, material, dimensionsMm, palettes et personalizationSchema |
| ProductImage | src local ou autorisé, alt et isDemo |
| Palette | id stable, label et colors de longueur 2 à 4 pour les produits multicolores initiaux |
| Personalization | objet discriminé par kind, avec version=1, options et paletteId selon le produit |
| CartLine | productId, personalization, quantity et prix affiché issu du catalogue |
| Order | id, reference, customer, items, subtotalCents, shippingCents, totalCents, currency, paymentMethod='cod', status et createdAt |
| OrderItem | productId, productNameSnapshot, quantity, unitPriceCents, personalizationSnapshot et lineTotalCents |
| Quote | id, reference, nom, téléphone, ville, type de projet, description, quantité, palette souhaitée, statut et createdAt |

Product.status vaut demo, draft, active ou archived. La boutique démo peut exposer demo avec un avertissement. Le mode commandes expose les active. Une dimension inconnue est null et la fiche le signale.

Pour kind=name, définir language='fr'|'ar'|'both', frenchName, arabicName et paletteId. Les graphies requises sont renseignées selon le mode. Préserver le texte entré, mesurer 1–24 graphèmes hors espaces de bord et laisser les chaînes inactives à null.

Pour kind=text, prévoir text et paletteId. Pour kind=qr, prévoir url et paletteId. Pour kind=none, interdire les champs de personnalisation. Les produits dont le besoin dépasse le schéma passent en devis. L’URL QR est une URL HTTPS de longueur au plus 2 048 caractères. La traiter comme donnée à imprimer et comme lien explicitement ouvert par l’utilisateur.

Les montants sont des entiers positifs ou nuls, les quantités des entiers de 1 à 99. Les limites des champs sont exposées aux formulaires et revérifiées au serveur.

## 3. Recherche, modèle et produit sont liés

| Contrat interne | Usage et champs |
| --- | --- |
| SourceObservation | id, sourceSite, externalId nullable, sourceUrl, originalUrl nullable, observedAt, observationStatus, notes |
| ModelRecord | id, sourceObservationId, creator, licenceLabel, licenceUrl, permissions, reviewStatus et rightsEvidenceRef |
| ModelAsset | id, modelId, version, format, privateStorageKey, sha256 et acquiredAt |
| ManufacturingData | productId, modelAssetId nullable, material, dimensionsMm, filamentGrams, purgeGrams, printHours, colorCount, supportRequired, productionCostCents, slicedAt et prototypeStatus |
| RightsReview | modelId, reviewer, reviewedAt et preuves d’impression commerciale, modification, redistribution et médias |

Les permissions impression commerciale, modification et redistribution sont séparées, chacune true, false ou null. reviewStatus vaut needs_review, approved ou rejected. L’approbation d’impression n’implique aucune autorisation de publier le fichier numérique. Une conception originale possède aussi un auteur et une référence de propriété.

La publication d’un produit active dépend de la revue des droits du modèle et des médias, d’un prototype validé et d’un prix commercial confirmé. Pour les six démos actuelles, conserver des visuels originaux de démonstration et un statut demo.

Les coûts, les clés de stockage, les preuves et les observations ne font pas partie des DTO publics. Définir un mapping explicite des champs autorisés.

## 4. Source de données locale

Garder un catalogue TypeScript local unique dans la démo. Centraliser getProducts et getProductBySlug dans un module serveur réutilisé par les pages et la future API. Envoyer aux composants clients uniquement les produits/champs publics nécessaires.

Lire DEMO_MODE côté serveur et choisir la démo si la variable manque ou diffère de la chaîne false. Renvoyer aux composants un simple indicateur public calculé par le serveur. Le futur mode commandes reste fermé tant que sa configuration requise est incomplète.

## 5. PostgreSQL au jalon commandes

Utiliser PostgreSQL avec pg et des migrations SQL numérotées. Créer products, source_observations, model_records, model_assets, product_models, manufacturing_data, orders, order_items, quotes et schema_migrations. Ajouter une table de limitation de débit lors du raccordement public des écritures.

- Identifiants UUID générés côté application pour les commandes, devis et enregistrements de recherche. Conserver les IDs texte du catalogue existant.
- Colonnes structurées pour états, montants, identifiants, dates et relations. TIMESTAMPTZ en UTC pour les événements.
- JSONB pour les options variables et les instantanés de personnalisation, avec validation côté application et CHECK sur la forme attendue.
- PRIMARY KEY, NOT NULL, UNIQUE et FOREIGN KEY selon les relations. CHECK pour montants, quantités, couleur et états.
- Unicité de sourceUrl, unicité partielle sourceSite/externalId lorsque externalId existe, et unicité de la clé d’idempotence des commandes.
- Index sur slug, orders.created_at, order_items.order_id et les clés étrangères fréquemment consultées. Ajouter les autres index après examen d’une requête réelle.
- Prix et quantités en colonnes entières. Vérifier le total inter-lignes dans la transaction d’écriture.
- Archivage des produits et modèles liés à des commandes, avec conservation des instantanés historiques.
- Une transaction par migration et un verrou de migration pour empêcher deux exécutions concurrentes.
- Seed idempotent des six produits par id, avec séparation des données de démonstration et réelles.

Le runtime Next.js accède à la base uniquement côté serveur avec DATABASE_URL. Les migrations utilisent une connexion dédiée et le runtime des permissions limitées aux opérations nécessaires. Les preuves et fichiers restent en stockage privé.

Les contraintes relationnelles et JSONB suivent la documentation officielle. [Contraintes PostgreSQL](https://www.postgresql.org/docs/current/ddl-constraints.html) · [JSONB PostgreSQL](https://www.postgresql.org/docs/current/datatype-json.html)

## 6. Import et évolution

Importer les observations de recherche dans une commande administrative locale avec prévisualisation. Les imports sont répétables, les preuves déjà vérifiées sont conservées et une nouvelle observation contradictoire déclenche une revue. Une importation de liens ne crée pas automatiquement des produits active.

Versionner Personalization et CartLine. Lors d’une évolution, prévoir une conversion explicite des versions supportées et un traitement clair des versions inconnues. Les anciens OrderItem gardent leur instantané d’origine.

## 7. Acceptation

- Les six URLs, prix indicatifs et graphies fonctionnent après migration des types.
- Les DTO publics excluent les coûts, preuves et fichiers privés.
- La démo démarre sans base et refuse les écritures.
- Au jalon PostgreSQL, appliquer les migrations sur base vide et sur base déjà migrée.
- Tester les contraintes, la déduplication d’import et le seed répété.
- Tester une ligne de commande historique après changement d’un produit.
- Exécuter TypeScript et le build, puis relire les migrations avec postgresql-code-review si le skill est disponible.
```

## Fichier prompts/backend/02-commandes-et-devis.md

```markdown
# Backend 02 — Catalogue, commandes et devis

## Mission et ordre

Implémente les routes dans le même projet Next.js avec les contrats Backend 01. Premier sous-jalon, GET catalogue et refus des écritures démo. Le traitement PostgreSQL et les formulaires réels constituent le sous-jalon commandes local.

Utiliser le runtime Node.js pour les accès pg et la validation partagée des entrées, avec Zod pour le jalon commandes. Le catalogue est lu côté serveur et possède un mapping public explicite.

## 1. Interfaces

| Route | Entrée | Résultat |
| --- | --- | --- |
| GET /api/products | Aucun paramètre requis | 200 avec produits publics selon le mode |
| POST /api/orders | items, customer, note facultative et en-tête Idempotency-Key | 201 avec référence, devise et totaux après écriture |
| POST /api/quotes | coordonnées et description du projet | 201 avec référence après écriture |

Une ligne items contient productId, quantity et personalization. Le client ne choisit ni prix ni statut. Le serveur charge les produits actifs, valide leurs options et calcule toutes les valeurs.

En mode démo, POST orders et quotes renvoient 403 avec code DEMO_MODE avant de lire le corps ou de contacter la base. Le frontend reçoit « Commandes bientôt disponibles ». Garder le GET fonctionnel sans PostgreSQL.

## 2. Validation du jalon commandes

- Requêtes JSON de 32 Ko maximum et listes orders de 1 à 20 lignes.
- Nom et ville de 2 à 120 caractères, adresse de 5 à 500 et note au plus 1 000.
- Téléphone marocain mobile saisi sous 06/07, +2126/+2127 ou 002126/002127, avec espaces, tirets et parenthèses autorisés. Normaliser en +212 suivi de neuf chiffres commençant par 6 ou 7.
- Quantité entière de 1 à 99 par ligne et devis.
- Texte de projet de 10 à 4 000 caractères et type issu d’une liste contrôlée.
- Toutes les personnalisations utilisent le schéma du produit côté serveur.
- Lignes, propriétés et options inconnues produisent une erreur de validation.

Appliquer les frais de livraison issus d’une configuration commerciale validée par ville. Tant que cette configuration manque, garder le mode démo. Les prix reçus du client sont rejetés. Présenter les totaux serveur avant confirmation d’une commande.

## 3. Écriture atomique et nouvelle tentative

1. Valider le JSON et les coordonnées.
2. Calculer une empreinte du contenu canonique accepté, dans un ordre stable de propriétés. Inclure toutes les coordonnées, lignes et options qui définissent la demande.
3. Dans une transaction, réserver la clé d’idempotence unique, lire les produits en protégeant le prix utilisé, calculer et conserver les totaux et instantanés, puis insérer les lignes.
4. En cas de course sur la même clé, lire l’enregistrement validé par l’autre transaction. Une empreinte identique donne 200 avec sa référence et ses totaux.
5. Une empreinte différente sur la même clé donne 409.
6. En cas de panne avant commit, rollback complet et réponse de panne. Le client peut reprendre la même clé.
7. Une modification du panier ou des coordonnées génère une nouvelle clé côté client.

Les devis utilisent eux aussi une clé unique et une empreinte pour éviter un doublon sur nouvelle tentative. Les confirmations sont privées, sans endpoint public permettant d’énumérer les commandes.

## 4. Erreurs et exploitation

Utiliser 400 pour JSON invalide, 413 pour corps trop grand, 415 pour type de contenu incorrect, 422 pour champs ou produits indisponibles, 409 pour clé conflictuelle, 429 pour débit et 503 pour stockage indisponible.

Avant l’activation publique, limiter les POST à cinq essais par dix minutes et par clé de client dérivée du réseau, avec compteur PostgreSQL partagé. Documenter l’en-tête proxy fiable de l’hébergement, utiliser une empreinte réseau courte durée et éviter l’adresse brute dans les logs. Une vérification d’origine same-origin complète la protection des formulaires.

Les logs contiennent code d’erreur, référence technique et durée. Garder téléphone, nom, adresse, contenu de personnalisation et corps HTTP hors des logs. Masquer les traces de base de données dans les réponses.

## 5. Recette

- Produit inexistant ou archivé, palette inconnue, personnalisation vide et quantité hors limites refusés.
- Prix falsifié rejeté et totaux serveur cohérents avec les frais configurés.
- Deux tentatives identiques, y compris simultanées, créent une seule commande.
- Même clé avec contenu différent donne 409.
- Panne pendant l’insertion d’une ligne laisse une transaction annulée.
- Une commande garde son instantané après modification du catalogue.
- Redémarrage du serveur conserve les commandes en PostgreSQL.
- Mode démo renvoie 403 sans ouvrir de connexion et sans lire de coordonnées.
- GET catalogue exclut fabrication et preuves internes.
```

## Fichier prompts/backend/03-railway-et-recette.md

````markdown
# Backend 03 — Recette locale et publication Railway ultérieure

## Mission actuelle

Vérifie la démo MustDesign3D en local. Le propriétaire a demandé de terminer les vérifications locales avant toute publication. Ce prompt prépare Railway pour une demande ultérieure.

## 1. Vérification technique locale

1. Utiliser Node 22.x selon package.json et npm.cmd ci selon le lockfile.
2. Exécuter npm.cmd run typecheck puis npm.cmd run build.
3. Démarrer une session de production sur un port libre.

```powershell
$env:PORT = '3138'
$env:DEMO_MODE = 'true'
npm.cmd start
```

Tester sur http://localhost:3138. Le script existant next start --hostname 0.0.0.0 utilise PORT. Arrêter cette session avec Ctrl+C avant de relancer le même port. Le mode développement passe par npm.cmd run dev -- --port 3138.

## 2. Recette navigateur

- GET accueil, catalogue, contact, six fiches, pages projet et récapitulatif. Une fiche inconnue donne 404.
- Recherche, filtres combinés, navigation arrière, tri et état sans résultat.
- Français, arabe et bilingue, direction du texte, saisie invalide, graphème long et palette.
- Ajout, fusion, modification, retrait, total et restauration du panier après rechargement.
- Modal accessible au clavier, Échap et retour de focus.
- Largeurs 320, 390 et 1440 px, absence de débordement, images de repli et contact à configurer.
- Démo sans coordonnées et refus serveur des écritures lorsqu’elles existent.
- Vérifier que chaque média et nouveau produit possède le statut de vérification attendu.

Au jalon PostgreSQL local, compléter par les essais de migrations, contraintes, doublons et pannes de Backend 01/02. Utiliser des coordonnées synthétiques.

## 3. Rapport de fin de recette

Lister les commandes exécutées et résultats, routes vérifiées, tailles d’écran, erreurs éventuelles et points métier à confirmer. Garder une distinction explicite entre une fonctionnalité testée et une fonctionnalité prévue dans les prompts.

## 4. Publication après demande explicite

Revalider l’offre et l’usage du workspace Railway au moment de la publication. Employer un seul service Next.js pour la démo et le catalogue local. L’adresse de service Railway est générée depuis les paramètres réseau. Les domaines MustDesign3D.com et MustDesign3D.ma restent des choix d’enregistrement.

Dans le dossier du projet, vérifier d’abord railway status et relier le projet du propriétaire. Créer un projet seulement si aucun projet adapté n’existe. L’ancien nom partagé était feisty-upliftment, identifiant 03615c2c-7612-46ab-ae45-372506115457, à revalider par les outils Railway avant utilisation.

Configurer DEMO_MODE=true dans le service. Réutiliser railway.toml avec npm run build, npm start et healthcheck /. Déployer avec la CLI seulement lorsque la publication est demandée, puis attendre l’état sain, générer le domaine et vérifier les routes HTTPS.

La documentation Railway fournit les options de déploiement Next.js et le raccordement PostgreSQL. [Guide officiel](https://railway.com/guides/nextjs)

## 5. Crédit et persistance

Consulter les plafonds et le crédit dans Usage avant publication, puis après une journée de trafic de démo. L’hébergement dépend de la consommation des ressources. En cas d’épuisement, conserver une démonstration locale utilisable.

Lors de la future ouverture des commandes, créer un environnement séparé et un PostgreSQL, référencer DATABASE_URL côté serveur par le réseau privé et appliquer les migrations avant de changer le mode. Vérifier sauvegarde/restauration et consultation des commandes par l’atelier. Les données persistantes utilisent PostgreSQL, et les médias/fichiers autorisés un stockage adapté.

Valider prix, frais/zones de livraison, coordonnées, droits des modèles et traitement quotidien des commandes avant activation du COD.
````

## Fichier prompts/frontend/01-fondations-et-accueil.md

```markdown
# Frontend 01 — Identité et accueil MustDesign3D

## Mission et entrées

Lis prompts/00-master-mustdesign3d.md et recherche/01-sources-et-selection.md. Développe la prochaine version de l’accueil dans le projet existant. Vérifie app/layout.tsx, app/page.tsx, app/globals.css et app/cart.tsx avant de modifier la navigation.

## Livrables

1. Une identité MustDesign3D cohérente dans les titres, métadonnées, navigation, états vides et pied de page.
2. Une barre de contact avec accès à /contact et au panier, lisible à 320 px.
3. Un menu pour la boutique, les collections, les projets professionnels et le contact.
4. Un accueil avec visuel principal, trois vedettes, catégories, étapes de personnalisation, section atelier, section professionnelle et FAQ.
5. Des liens vers /shop, les six fiches existantes, /custom et /business au fur et à mesure de leur création.
6. Un composant de configuration publique de la marque et des coordonnées pour éviter la duplication.

## Direction visuelle

Fond ivoire, surface sable, texte anthracite, bleu Majorelle pour les actions, hiérarchie typographique expressive et photos lisibles. Conserver une composition mobile compacte et des sections distinctes. Varier l’échelle du produit vedette et des cartes.

S’inspirer des catégories To7fa et de l’explication produit 3DGIFI, puis écrire les textes et produire les visuels MustDesign3D. Une illustration de démonstration porte une légende et une photo possède un texte alternatif adapté.

## Comportement

- Garder MustDesign3D comme nom visible. Le domaine retenu sera une configuration fournie après enregistrement.
- Conserver les trois vedettes, porte-clés prénom, plaque de bureau et support QR.
- Afficher les liens téléphone, email ou WhatsApp uniquement quand le propriétaire fournit une valeur réelle et valide.
- Afficher l’état d’attente des coordonnées sur /contact tant qu’elles manquent.
- Centraliser les libellés français pour faciliter une traduction arabe ultérieure.
- Utiliser des propriétés CSS logiques et des zones dir="auto" pour le texte saisi.
- Les délais, garanties, avis et prix commerciaux publiés proviennent des validations de l’atelier.
- Conserver l’indication de démo tant que les commandes restent fermées.

## Réutilisation et qualité

Conserver Next.js App Router, TypeScript et Tailwind. Réutiliser ProductCard, ProductArt et le fournisseur de panier quand leurs contrats conviennent. Garder les interactions dans les composants clients concernés et les pages de contenu côté serveur.

## Acceptation

- Navigation, contact, boutique et fiches accessibles au clavier.
- À 320, 390 et 1440 px, liens lisibles, boutons utilisables et aucun débordement horizontal.
- Le lien d’évitement fonctionne et les images ont des alternatives adaptées.
- Les coordonnées d’un concurrent restent dans la recherche.
- TypeScript et build réussis. Fournir captures mobile/desktop et liste des liens vérifiés lors de l’implémentation.
```

## Fichier prompts/frontend/02-catalogue-et-personnalisation.md

```markdown
# Frontend 02 — Catalogue, fiches et personnalisation

## Mission et dépendances

Après Backend 01 en mode démo et Frontend 01, enrichis /shop et /product/[slug]. Lis les types partagés avant de toucher aux props de ProductCard, au prix ou aux lignes de panier.

## Catalogue

- Conserver les six slugs existants et leurs prix indicatifs.
- Présenter les quatre collections actuelles, Cadeaux, Maison & bureau, Professionnels, Décoration.
- Rendre la recherche insensible à la casse et aux accents pour le français.
- Combiner recherche et catégorie, afficher le nombre de résultats et un bouton de réinitialisation.
- Représenter le filtre et la recherche dans les paramètres URL pour partager une collection et rétablir la navigation arrière.
- Proposer un tri par mise en avant et par prix. Conserver une option claire pour tous les produits.
- Les candidats du registre recherche restent dans les documents internes. Ajouter uniquement des fiches ayant un contenu et un statut démo ou validé explicite.

## Fiche produit

Prévoir galerie, titre, description originale, prix en MAD, choix applicables, quantité, détail des dimensions/matériau, modalités de démo et produits associés. Préserver la 404 pour un slug inconnu. Afficher une illustration locale de repli si un média manque.

Produire des métadonnées adaptées à la fiche. Ajouter Product/Offer dans les données structurées uniquement lorsque les informations de vente sont effectivement validées.

## Personnalisation du porte-clés

- Modes français, arabe et bilingue, avec un champ pour chaque graphie en mode bilingue.
- Pour chaque graphie requise, de 1 à 24 graphèmes hors espaces en début/fin. Réutiliser la même validation de part et d’autre du contrat.
- Conserver l’écriture de l’utilisateur. Utiliser dir="auto" et une police assurant la liaison des lettres arabes.
- Trois palettes de départ issues du configurateur actuel, avec identifiant stable et deux, trois ou quatre couleurs.
- Quantité entière de 1 à 99.
- Désactiver l’ajout tant qu’un champ requis ou une quantité est incorrect. Associer le message de correction au champ.
- Générer un aperçu 2D reflétant la palette et les graphies saisies.
- Mentionner les dimensions indicatives 65–85 mm de large et 3–4 mm d’épaisseur.
- Garder les choix lorsque le client ouvre et referme le panier.
- Toute limite d’impression réelle liée à la longueur du prénom passe par la validation de production ultérieure.

## Autres fiches

Déclarer les champs nécessaires par produit. Les noms, ville, texte professionnel et URL QR utilisent des options typées. Si une fiche nécessite un logo ou une étude spécifique, orienter vers /custom avec le produit présélectionné. Le jalon initial ne comporte pas de dépôt de fichier. Les dimensions et caractéristiques inconnues restent à confirmer.

## Acceptation

Tester un prénom latin accentué, un prénom arabe, les deux graphies, une saisie vide, la limite de longueur, le changement de mode et chaque palette. Vérifier la recherche sans résultat, le retour arrière, les filtres combinés, le prix indicatif et les URLs produit.

Vérifier au clavier et aux trois largeurs définies dans le guide. Les nouveaux produits utilisent les mêmes composants et formats de prix.
```

## Fichier prompts/frontend/03-panier-et-parcours-client.md

```markdown
# Frontend 03 — Panier et parcours démo

## Mission

Après les deux premiers prompts frontend et les contrats partagés, complète le panier latéral déjà présent dans app/cart.tsx. Garde la fiche produit comme entrée de personnalisation.

## Panier

1. Utiliser le contrat CartLine versionné et les identifiants stables des produits et options.
2. Fusionner uniquement les lignes ayant le même produit et la même personnalisation.
3. Permettre la quantité 1–99, le retrait et un lien « Modifier » vers la fiche avec les options restaurées.
4. Mémoriser dans localStorage les produits/options/quantités avec schemaVersion. Restaurer après hydratation pour éviter une divergence serveur/client.
5. Relire le prix du catalogue courant lors de la restauration et signaler un produit retiré ou des options devenues indisponibles.
6. Prévoir un localStorage indisponible, un JSON invalide ou une version inconnue. Revenir à un panier mémoire utilisable avec une information compréhensible.
7. Afficher le sous-total en MAD et indiquer que les frais et délais seront précisés à l’ouverture.
8. Afficher des produits complémentaires au prix du catalogue. Garder la personnalisation requise via un lien vers la fiche.
9. Assurer focus initial, focus contenu dans le dialogue, fermeture Échap et retour du focus au déclencheur.

Le panier actuel possède des lignes à détails textuels en mémoire. Les reconstruire avec les options typées avant d’ajouter l’édition. Les deux graphies d’une ligne bilingue restent distinctes.

## Pages à livrer

- /checkout, récapitulatif du panier et « Commandes bientôt disponibles » avant tout champ de coordonnées.
- /custom, exemples et explication des informations à préparer, sans collecte en mode démo.
- /business, exemples de plaques, supports et petites séries avec lien vers /custom.
- /contact, coordonnées de configuration et état d’attente lorsqu’elles sont absentes.

Le bouton de poursuite du panier ouvre /checkout. En démo, le libellé annonce « Voir le récapitulatif ». L’ajout ou la suppression d’un article ne simule pas l’envoi d’une commande.

## Jalon commandes ultérieur

Quand Backend 02 et la validation commerciale sont terminés, remplacer le verrou visuel par les formulaires COD/devis. Le formulaire COD demande nom, téléphone marocain, ville, adresse et note facultative. Le devis demande nom, téléphone, ville, type de projet, description, quantité et couleurs.

Reprendre la clé d’idempotence lors d’une nouvelle tentative du même envoi. Une modification du contenu constitue une nouvelle demande. La confirmation affiche uniquement une référence obtenue après écriture serveur réussie.

## Acceptation

Tester deux personnalisations différentes, fusion de lignes identiques, quantité maximale, retrait, modification puis rechargement. Tester restauration corrompue et stockage indisponible. Vérifier la conservation du prénom arabe, la navigation clavier et l’absence de collecte de coordonnées en démo.
```

## Fichier prompts/handoff/COPILOT_MASTER.md

```markdown
# Version GitHub Copilot — Développer MustDesign3D

## Mode d’emploi

Ouvrir la racine du projet dans VS Code et ajouter ce fichier au contexte du chat Copilot en mode agent. Ajouter MASTER_PROJECT.md et les fichiers du lot concerné. Si le code est seulement disponible dans un autre chat, joindre PROJECT_SOURCE.md.

Les instructions persistantes de dépôt peuvent être placées dans .github/copilot-instructions.md après lecture des instructions existantes. Ce paquet fournit des prompts portables à joindre et laisse la configuration locale à son propriétaire.

Un modèle Gemini peut être sélectionné dans Copilot lorsqu’il est proposé par le compte. Les outils de fichiers et de terminal dépendent de l’éditeur. Les images demandent un service de génération dédié ou les prompts à transmettre au propriétaire.

## Plan Copilot

1. Lire les fichiers du projet et identifier les points d’entrée existants.
2. Pour un lot UI, vérifier Product, ProductImage, le catalogue serveur et les composants consommateurs.
3. Pour un lot de personnalisation, vérifier le validateur partagé, la restauration du panier et l’édition.
4. Développer le plus petit changement complet puis contrôler l’intégration par les routes habituelles.
5. Exécuter npm run typecheck et npm run build, puis les scénarios de navigateur.
6. Régénérer le paquet de contexte avec npm run handoff.
7. Donner un résumé des changements, des tests, des blocages concrets et des tâches restantes.

## Prompt à lancer

> Lis ce fichier et MASTER_PROJECT.md. Examine le projet réel, puis réalise le prochain lot P0 compatible avec l’état local. Réutilise les composants et contrats existants, préserve les anciennes URLs et compositions, et ajoute les validations nécessaires aux nouveaux champs. Exécute les vérifications disponibles et rapporte leurs résultats. Garde la distinction entre concepts, prototypes et produits vendables.

---

# MustDesign3D — Prompt maître du projet

## Mission

Tu reprends le développement de MustDesign3D, une marque marocaine d’objets personnalisés imprimés en 3D. Travaille dans le projet existant en lisant les fichiers réels avant une modification. Utilise ce prompt avec PROJECT_SOURCE.md si tu n’as pas accès au dossier du projet.

Le propriétaire veut une vitrine proche de la structure du catalogue To7fa, avec une identité et des créations MustDesign3D. La cible initiale est le Maroc, en français, avec personnalisation arabe et bilingue. La devise est MAD.

## État fonctionnel attendu et architecture

En cas d’écart entre les documents, suivre la demande actuelle du propriétaire et ce contexte de reprise, puis vérifier le code réel. Les recherches et anciens prompts restent des références datées.

Next.js App Router, React, TypeScript strict, Tailwind, Node 22.x. Le lockfile fixe les versions installées. Le catalogue autoritaire est côté serveur, les options et le panier ont des contrats TypeScript partagés. Les montants sont des centimes entiers. pricingMode=quote donne priceCents=null et le libellé « Sur devis ».

Routes, /, /shop, /product/[slug], /modeles, /custom, /business, /contact, /checkout, /api/products, /api/orders et /api/quotes.

Le site reste en mode démo local. Les routes POST commandes/devis renvoient 403 DEMO_MODE avant lecture du corps. Le panier est une composition locale conservée dans localStorage avec validation à la restauration.

## Sélection commerciale

| Collection | Référence | Prix indicatif |
| --- | --- | --- |
| Cadeaux personnalisés | Porte-clés prénom | 49 MAD |
| Cadeaux personnalisés | Porte-clés plaque marocaine | 45 MAD |
| Cadeaux personnalisés | Étiquette de sac | 39 MAD |
| Cadeaux personnalisés | Marque-places, lot de dix | Sur devis |
| Maison & bureau | Plaque de bureau | 99 MAD |
| Maison & bureau | Plaque de porte | 99 MAD |
| Professionnels | Présentoir QR | 149 MAD |
| Professionnels | Plaque de contact | 99 MAD |
| Professionnels | Porte-clés logo en lot | Sur devis |

Trois vedettes, porte-clés prénom, plaque de bureau et QR. La skyline, la plaque pixel et le gabarit logo de bureau sont conservés comme prototypes. Les neuf fiches sont des concepts de catalogue, sept modèles CAD existent pour les études historiques. Vérifier la correspondance entre une fiche, son modèle et ses médias.

Ces prix servent à la démonstration. Calculer matière, purge, temps, travail, emballage et livraison avant une validation commerciale.

## Direction artistique

Fond ivoire, sable, anthracite et accent bleu Majorelle. Filaments de départ bleu, noir, blanc et rouge, deux couleurs préférées. La couleur du décor photographique est indépendante de celle du produit.

Catalogue avec recherche, trois collections, filtres latéraux sur ordinateur, panneau accessible sur mobile, prix/devis lisibles et cartes 4:5. Prévoir quatre colonnes sur grand écran et une densité adaptée aux tailles intermédiaires.

La boutique privilégie des médias commerciaux approuvés. Les aperçus CAD restent dans la galerie technique. Tant que les nouvelles images manquent, les illustrations originales du concept portent leur légende.

## Personnalisation et compatibilité

Conserver les six anciens slugs et les identifiants stables. Les prénoms français/arabe/bilingue ont une validation en graphèmes. Conserver la graphie, les accents et la liaison des lettres arabes.

Garder les noms, options et quantités du panier à travers les évolutions. Signaler clairement toute palette adaptée ou référence passée sur devis. L’ancien panier version 1 reste lisible.

Le QR doit encoder le lien HTTPS exact sans visite automatique de ce lien. Préserver la zone calme et le contraste. La vérification sur écran et le test de la pièce imprimée sont deux étapes distinctes.

Les références de petites séries passent par le parcours projet. L’ouverture des devis réels nécessitera un backend et une configuration commerciale.

## Fabrication et provenance

Machine A1 avec AMS Lite et quatre filaments. Viser une enveloppe conservatrice de 220 mm, une impression plate et peu de changements de couleur. Les réglages 0,4 mm / 0,20 mm / PLA sont un point de départ d’essai.

Les fichiers privés sont sous production/. Les images publiques sont des assets distincts. Enregistrer auteur, source, licence, permissions d’impression/modification/redistribution, version et SHA256 du modèle. Le guide MakerWorld fourni décrit le modèle d’Alberto Nicás v2.9, mais ses fichiers et conditions restent à acquérir.

Les pages To7fa, 3DGIFI, SliSearch et la liste A1_100_Product_References.md servent à la recherche. Une fiche commerciale et une requête de recherche de modèle apportent des informations différentes. Confirmer les droits de chaque fichier acquis.

## Photos et concepts générés

Avant une nouvelle série d’images, corriger la géométrie et choisir la version de produit à représenter. Générer une paire pilote, porte-clés et présentoir QR, puis évaluer formes, textes, dimensions apparentes et couleurs.

Médias possibles, photo, generated-concept ou cad-preview. Une image générée porte « Visualisation du concept ». Remplacer progressivement les vues commerciales par des photos de prototypes validés.

Un modèle de programmation Gemini sélectionné dans un éditeur travaille sur le code. La génération d’images nécessite un outil ou service d’image disponible dans l’environnement. Vérifier cette capacité et le crédit de génération avant le lot pilote.

## Séquence de travail

1. Lire ce document, l’état de livraison dans README.md et le plan de refonte.
2. Examiner les contrats, le catalogue, le panier et les composants qui affichent les médias.
3. Choisir un lot de travail parmi les tâches restantes, avec un résultat vérifiable.
4. Développer le lot en préservant les comportements existants.
5. Exécuter TypeScript, build et les scénarios navigateur adaptés.
6. Mettre à jour le README et régénérer PROJECT_SOURCE.md après les modifications.
7. Rapporter les fichiers modifiés, les tests réellement exécutés, les limites et la prochaine étape.

## Tâches suivantes prioritaires

- P0, corriger le porte-clés en contour et préparer une véritable version de production du QR. Associer une géométrie et une preuve de validation aux nouvelles références.
- P0, produire et approuver les deux images conceptuelles pilotes avant les vingt-sept vues de produits.
- P0, photographier les prototypes et mesurer les coûts réels.
- P1, ajouter la deuxième ligne des plaques et les champs structurés de plaque marocaine.
- P1, ajouter le nom du commerce et le type de destination du QR.
- P1, préparer une variante double face du porte-clés après contrôle d’assemblage.
- P2, ajouter le suivi de stock de filaments et un tableau de production simple.
- P2, étudier PostgreSQL, commandes COD et devis réels après validation du parcours démo.

## Contrôle de livraison

TypeScript et build réussis. Vérifier 320, 390, 768, 1024 et 1440 px, clavier, filtre mobile, recherche/tri/URL, panier, données corrompues et anciens formats. Une référence sur devis ne doit pas devenir un article à prix nul dans le panier. Le QR encodé se décode vers le lien exact.

Garder codex.md et les documents reçus comme références. Les snapshots joints sont en lecture seule. Toute publication Railway et tout achat de domaine nécessitent une demande ultérieure explicite du propriétaire.


## Source d’utilisation Copilot

La documentation GitHub décrit les instructions de dépôt et leurs fichiers de contexte. [Instructions personnalisées Copilot](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/add-custom-instructions/add-repository-instructions)
```

## Fichier prompts/handoff/GEMINI_MASTER.md

```markdown
# Version Gemini — Reprendre MustDesign3D

## Mode d’emploi

Dans Gemini CLI, ouvrir le projet puis donner ce fichier comme contexte. Si une instruction persistante est souhaitée, placer une copie de la section maître dans un GEMINI.md du projet après examen des instructions existantes. Dans une interface de chat, joindre ce fichier et PROJECT_SOURCE.md. Les assets binaires sont décrits par le manifeste du snapshot et fournis séparément si nécessaire.

Gemini peut être utilisé pour analyser le produit, coder et produire les briefs photo. La génération d’images demande une capacité dédiée, par exemple le service d’image Gemini disponible dans Google AI Studio ou une intégration Runway connectée.

## Plan Gemini

1. Lire le contexte et dresser l’état réel du code. Repérer ce qui est déjà testé et ce qui reste une proposition.
2. Préparer une fiche pour chacune des neuf références, besoin, modèle/version, options, couleurs et statut de validation.
3. Sélectionner les trois produits vedettes et corriger leur géométrie avant toute génération visuelle.
4. Préparer deux essais d’image à partir de références approuvées, avec les prompts photo joints.
5. Contrôler l’image face à la référence et garder les échecs de typographie ou géométrie à reprendre.
6. Coder un lot ciblé dans le projet lorsque l’environnement permet l’édition. Dans le mode chat, donner des changements complets par fichier et des commandes de vérification reproductibles.
7. Mettre à jour les documents et le snapshot après exécution.

## Prompt à lancer

> Agis comme mon agent produit et développeur pour MustDesign3D. Commence par analyser le contexte ci-dessous et les fichiers joints. Identifie le prochain lot P0 réalisable, donne brièvement son résultat attendu puis développe-le dans le projet si tes outils le permettent. Distingue les sources consultées, les hypothèses et les vérifications exécutées. Pour les images, utilise les références du produit et le service réellement disponible. Respecte les invariants de démo et de compatibilité.

---

# MustDesign3D — Prompt maître du projet

## Mission

Tu reprends le développement de MustDesign3D, une marque marocaine d’objets personnalisés imprimés en 3D. Travaille dans le projet existant en lisant les fichiers réels avant une modification. Utilise ce prompt avec PROJECT_SOURCE.md si tu n’as pas accès au dossier du projet.

Le propriétaire veut une vitrine proche de la structure du catalogue To7fa, avec une identité et des créations MustDesign3D. La cible initiale est le Maroc, en français, avec personnalisation arabe et bilingue. La devise est MAD.

## État fonctionnel attendu et architecture

En cas d’écart entre les documents, suivre la demande actuelle du propriétaire et ce contexte de reprise, puis vérifier le code réel. Les recherches et anciens prompts restent des références datées.

Next.js App Router, React, TypeScript strict, Tailwind, Node 22.x. Le lockfile fixe les versions installées. Le catalogue autoritaire est côté serveur, les options et le panier ont des contrats TypeScript partagés. Les montants sont des centimes entiers. pricingMode=quote donne priceCents=null et le libellé « Sur devis ».

Routes, /, /shop, /product/[slug], /modeles, /custom, /business, /contact, /checkout, /api/products, /api/orders et /api/quotes.

Le site reste en mode démo local. Les routes POST commandes/devis renvoient 403 DEMO_MODE avant lecture du corps. Le panier est une composition locale conservée dans localStorage avec validation à la restauration.

## Sélection commerciale

| Collection | Référence | Prix indicatif |
| --- | --- | --- |
| Cadeaux personnalisés | Porte-clés prénom | 49 MAD |
| Cadeaux personnalisés | Porte-clés plaque marocaine | 45 MAD |
| Cadeaux personnalisés | Étiquette de sac | 39 MAD |
| Cadeaux personnalisés | Marque-places, lot de dix | Sur devis |
| Maison & bureau | Plaque de bureau | 99 MAD |
| Maison & bureau | Plaque de porte | 99 MAD |
| Professionnels | Présentoir QR | 149 MAD |
| Professionnels | Plaque de contact | 99 MAD |
| Professionnels | Porte-clés logo en lot | Sur devis |

Trois vedettes, porte-clés prénom, plaque de bureau et QR. La skyline, la plaque pixel et le gabarit logo de bureau sont conservés comme prototypes. Les neuf fiches sont des concepts de catalogue, sept modèles CAD existent pour les études historiques. Vérifier la correspondance entre une fiche, son modèle et ses médias.

Ces prix servent à la démonstration. Calculer matière, purge, temps, travail, emballage et livraison avant une validation commerciale.

## Direction artistique

Fond ivoire, sable, anthracite et accent bleu Majorelle. Filaments de départ bleu, noir, blanc et rouge, deux couleurs préférées. La couleur du décor photographique est indépendante de celle du produit.

Catalogue avec recherche, trois collections, filtres latéraux sur ordinateur, panneau accessible sur mobile, prix/devis lisibles et cartes 4:5. Prévoir quatre colonnes sur grand écran et une densité adaptée aux tailles intermédiaires.

La boutique privilégie des médias commerciaux approuvés. Les aperçus CAD restent dans la galerie technique. Tant que les nouvelles images manquent, les illustrations originales du concept portent leur légende.

## Personnalisation et compatibilité

Conserver les six anciens slugs et les identifiants stables. Les prénoms français/arabe/bilingue ont une validation en graphèmes. Conserver la graphie, les accents et la liaison des lettres arabes.

Garder les noms, options et quantités du panier à travers les évolutions. Signaler clairement toute palette adaptée ou référence passée sur devis. L’ancien panier version 1 reste lisible.

Le QR doit encoder le lien HTTPS exact sans visite automatique de ce lien. Préserver la zone calme et le contraste. La vérification sur écran et le test de la pièce imprimée sont deux étapes distinctes.

Les références de petites séries passent par le parcours projet. L’ouverture des devis réels nécessitera un backend et une configuration commerciale.

## Fabrication et provenance

Machine A1 avec AMS Lite et quatre filaments. Viser une enveloppe conservatrice de 220 mm, une impression plate et peu de changements de couleur. Les réglages 0,4 mm / 0,20 mm / PLA sont un point de départ d’essai.

Les fichiers privés sont sous production/. Les images publiques sont des assets distincts. Enregistrer auteur, source, licence, permissions d’impression/modification/redistribution, version et SHA256 du modèle. Le guide MakerWorld fourni décrit le modèle d’Alberto Nicás v2.9, mais ses fichiers et conditions restent à acquérir.

Les pages To7fa, 3DGIFI, SliSearch et la liste A1_100_Product_References.md servent à la recherche. Une fiche commerciale et une requête de recherche de modèle apportent des informations différentes. Confirmer les droits de chaque fichier acquis.

## Photos et concepts générés

Avant une nouvelle série d’images, corriger la géométrie et choisir la version de produit à représenter. Générer une paire pilote, porte-clés et présentoir QR, puis évaluer formes, textes, dimensions apparentes et couleurs.

Médias possibles, photo, generated-concept ou cad-preview. Une image générée porte « Visualisation du concept ». Remplacer progressivement les vues commerciales par des photos de prototypes validés.

Un modèle de programmation Gemini sélectionné dans un éditeur travaille sur le code. La génération d’images nécessite un outil ou service d’image disponible dans l’environnement. Vérifier cette capacité et le crédit de génération avant le lot pilote.

## Séquence de travail

1. Lire ce document, l’état de livraison dans README.md et le plan de refonte.
2. Examiner les contrats, le catalogue, le panier et les composants qui affichent les médias.
3. Choisir un lot de travail parmi les tâches restantes, avec un résultat vérifiable.
4. Développer le lot en préservant les comportements existants.
5. Exécuter TypeScript, build et les scénarios navigateur adaptés.
6. Mettre à jour le README et régénérer PROJECT_SOURCE.md après les modifications.
7. Rapporter les fichiers modifiés, les tests réellement exécutés, les limites et la prochaine étape.

## Tâches suivantes prioritaires

- P0, corriger le porte-clés en contour et préparer une véritable version de production du QR. Associer une géométrie et une preuve de validation aux nouvelles références.
- P0, produire et approuver les deux images conceptuelles pilotes avant les vingt-sept vues de produits.
- P0, photographier les prototypes et mesurer les coûts réels.
- P1, ajouter la deuxième ligne des plaques et les champs structurés de plaque marocaine.
- P1, ajouter le nom du commerce et le type de destination du QR.
- P1, préparer une variante double face du porte-clés après contrôle d’assemblage.
- P2, ajouter le suivi de stock de filaments et un tableau de production simple.
- P2, étudier PostgreSQL, commandes COD et devis réels après validation du parcours démo.

## Contrôle de livraison

TypeScript et build réussis. Vérifier 320, 390, 768, 1024 et 1440 px, clavier, filtre mobile, recherche/tri/URL, panier, données corrompues et anciens formats. Une référence sur devis ne doit pas devenir un article à prix nul dans le panier. Le QR encodé se décode vers le lien exact.

Garder codex.md et les documents reçus comme références. Les snapshots joints sont en lecture seule. Toute publication Railway et tout achat de domaine nécessitent une demande ultérieure explicite du propriétaire.


## Sources d’utilisation Gemini

Le fonctionnement des fichiers de contexte est documenté par Gemini CLI. [Contexte GEMINI.md](https://geminicli.com/docs/cli/gemini-md/)

Pour les fonctions d’image, consulter les capacités et conditions en vigueur dans la documentation Google avant l’exécution du lot. [Génération d’images Gemini](https://ai.google.dev/gemini-api/docs/image-generation)
```

## Fichier prompts/handoff/MASTER_PROJECT.md

```markdown
# MustDesign3D — Prompt maître du projet

## Mission

Tu reprends le développement de MustDesign3D, une marque marocaine d’objets personnalisés imprimés en 3D. Travaille dans le projet existant en lisant les fichiers réels avant une modification. Utilise ce prompt avec PROJECT_SOURCE.md si tu n’as pas accès au dossier du projet.

Le propriétaire veut une vitrine proche de la structure du catalogue To7fa, avec une identité et des créations MustDesign3D. La cible initiale est le Maroc, en français, avec personnalisation arabe et bilingue. La devise est MAD.

## État fonctionnel attendu et architecture

En cas d’écart entre les documents, suivre la demande actuelle du propriétaire et ce contexte de reprise, puis vérifier le code réel. Les recherches et anciens prompts restent des références datées.

Next.js App Router, React, TypeScript strict, Tailwind, Node 22.x. Le lockfile fixe les versions installées. Le catalogue autoritaire est côté serveur, les options et le panier ont des contrats TypeScript partagés. Les montants sont des centimes entiers. pricingMode=quote donne priceCents=null et le libellé « Sur devis ».

Routes, /, /shop, /product/[slug], /modeles, /custom, /business, /contact, /checkout, /api/products, /api/orders et /api/quotes.

Le site reste en mode démo local. Les routes POST commandes/devis renvoient 403 DEMO_MODE avant lecture du corps. Le panier est une composition locale conservée dans localStorage avec validation à la restauration.

## Sélection commerciale

| Collection | Référence | Prix indicatif |
| --- | --- | --- |
| Cadeaux personnalisés | Porte-clés prénom | 49 MAD |
| Cadeaux personnalisés | Porte-clés plaque marocaine | 45 MAD |
| Cadeaux personnalisés | Étiquette de sac | 39 MAD |
| Cadeaux personnalisés | Marque-places, lot de dix | Sur devis |
| Maison & bureau | Plaque de bureau | 99 MAD |
| Maison & bureau | Plaque de porte | 99 MAD |
| Professionnels | Présentoir QR | 149 MAD |
| Professionnels | Plaque de contact | 99 MAD |
| Professionnels | Porte-clés logo en lot | Sur devis |

Trois vedettes, porte-clés prénom, plaque de bureau et QR. La skyline, la plaque pixel et le gabarit logo de bureau sont conservés comme prototypes. Les neuf fiches sont des concepts de catalogue, sept modèles CAD existent pour les études historiques. Vérifier la correspondance entre une fiche, son modèle et ses médias.

Ces prix servent à la démonstration. Calculer matière, purge, temps, travail, emballage et livraison avant une validation commerciale.

## Direction artistique

Fond ivoire, sable, anthracite et accent bleu Majorelle. Filaments de départ bleu, noir, blanc et rouge, deux couleurs préférées. La couleur du décor photographique est indépendante de celle du produit.

Catalogue avec recherche, trois collections, filtres latéraux sur ordinateur, panneau accessible sur mobile, prix/devis lisibles et cartes 4:5. Prévoir quatre colonnes sur grand écran et une densité adaptée aux tailles intermédiaires.

La boutique privilégie des médias commerciaux approuvés. Les aperçus CAD restent dans la galerie technique. Tant que les nouvelles images manquent, les illustrations originales du concept portent leur légende.

## Personnalisation et compatibilité

Conserver les six anciens slugs et les identifiants stables. Les prénoms français/arabe/bilingue ont une validation en graphèmes. Conserver la graphie, les accents et la liaison des lettres arabes.

Garder les noms, options et quantités du panier à travers les évolutions. Signaler clairement toute palette adaptée ou référence passée sur devis. L’ancien panier version 1 reste lisible.

Le QR doit encoder le lien HTTPS exact sans visite automatique de ce lien. Préserver la zone calme et le contraste. La vérification sur écran et le test de la pièce imprimée sont deux étapes distinctes.

Les références de petites séries passent par le parcours projet. L’ouverture des devis réels nécessitera un backend et une configuration commerciale.

## Fabrication et provenance

Machine A1 avec AMS Lite et quatre filaments. Viser une enveloppe conservatrice de 220 mm, une impression plate et peu de changements de couleur. Les réglages 0,4 mm / 0,20 mm / PLA sont un point de départ d’essai.

Les fichiers privés sont sous production/. Les images publiques sont des assets distincts. Enregistrer auteur, source, licence, permissions d’impression/modification/redistribution, version et SHA256 du modèle. Le guide MakerWorld fourni décrit le modèle d’Alberto Nicás v2.9, mais ses fichiers et conditions restent à acquérir.

Les pages To7fa, 3DGIFI, SliSearch et la liste A1_100_Product_References.md servent à la recherche. Une fiche commerciale et une requête de recherche de modèle apportent des informations différentes. Confirmer les droits de chaque fichier acquis.

## Photos et concepts générés

Avant une nouvelle série d’images, corriger la géométrie et choisir la version de produit à représenter. Générer une paire pilote, porte-clés et présentoir QR, puis évaluer formes, textes, dimensions apparentes et couleurs.

Médias possibles, photo, generated-concept ou cad-preview. Une image générée porte « Visualisation du concept ». Remplacer progressivement les vues commerciales par des photos de prototypes validés.

Un modèle de programmation Gemini sélectionné dans un éditeur travaille sur le code. La génération d’images nécessite un outil ou service d’image disponible dans l’environnement. Vérifier cette capacité et le crédit de génération avant le lot pilote.

## Séquence de travail

1. Lire ce document, l’état de livraison dans README.md et le plan de refonte.
2. Examiner les contrats, le catalogue, le panier et les composants qui affichent les médias.
3. Choisir un lot de travail parmi les tâches restantes, avec un résultat vérifiable.
4. Développer le lot en préservant les comportements existants.
5. Exécuter TypeScript, build et les scénarios navigateur adaptés.
6. Mettre à jour le README et régénérer PROJECT_SOURCE.md après les modifications.
7. Rapporter les fichiers modifiés, les tests réellement exécutés, les limites et la prochaine étape.

## Tâches suivantes prioritaires

- P0, corriger le porte-clés en contour et préparer une véritable version de production du QR. Associer une géométrie et une preuve de validation aux nouvelles références.
- P0, produire et approuver les deux images conceptuelles pilotes avant les vingt-sept vues de produits.
- P0, photographier les prototypes et mesurer les coûts réels.
- P1, ajouter la deuxième ligne des plaques et les champs structurés de plaque marocaine.
- P1, fait en démo locale : ajouter le nom de l’établissement et le type de destination du QR, conserver les compositions enregistrées et refléter le nom dans l’aperçu. La lecture sur pièce imprimée reste à valider.
- P1, préparer une variante double face du porte-clés après contrôle d’assemblage.
- P2, ajouter le suivi de stock de filaments et un tableau de production simple.
- P2, étudier PostgreSQL, commandes COD et devis réels après validation du parcours démo.

## Contrôle de livraison

TypeScript et build réussis. Vérifier 320, 390, 768, 1024 et 1440 px, clavier, filtre mobile, recherche/tri/URL, panier, données corrompues et anciens formats. Une référence sur devis ne doit pas devenir un article à prix nul dans le panier. Le QR encodé se décode vers le lien exact.

Garder codex.md et les documents reçus comme références. Les snapshots joints sont en lecture seule. Toute publication Railway et tout achat de domaine nécessitent une demande ultérieure explicite du propriétaire.
```

## Fichier prompts/handoff/PHOTO_PROMPTS.md

```markdown
# Brief photo — MustDesign3D pour Gemini ou un autre générateur

## Direction commune

Conserver la forme et les proportions du modèle de référence. Montrer du plastique FDM mat avec des stries fines et une lumière douce. Filaments de départ noir, blanc, bleu, rouge. Employer des noms et graphismes approuvés. Les décors peuvent utiliser bois clair, papier et tissu écru.

Le premier lot comprend deux images conceptuelles, une du porte-clés et une du présentoir QR. Valider cette paire avant de produire les trois vues des neuf références. Les neuf références totalisent vingt-sept images produit. L’accueil et les trois vues de collection apportent quatre médias supplémentaires.

Pour chaque fichier, consigner productId, version du modèle, couleur, type de vue, type de média, référence utilisée, outil et date. Le site affiche « Visualisation du concept » pour les concepts générés.

## Prompt 1 — Porte-clés en situation, 4:5

> Utiliser la référence approuvée du porte-clés prénom MustDesign3D. Conserver exactement son contour, son œillet, son épaisseur, le prénom et la typographie visibles sur la référence. Présenter le produit en FDM mat bleu et blanc sur une petite coupelle en bois clair, à côté de clés métalliques. Lumière de fenêtre douce, ombre de contact, proportions réalistes, stries fines d’impression, vue trois-quarts. Le porte-clés occupe la majorité de l’image. Préserver le nombre de couleurs et tous les détails du produit.

## Prompt 2 — Présentoir QR de comptoir, 4:5

> Utiliser la référence approuvée du présentoir MustDesign3D. Conserver le panneau, son support, leurs proportions et l’insertion du panneau. Montrer une face blanche, un graphisme noir et un support bleu, sur un comptoir de café sobre avec un arrière-plan légèrement flou. Lumière naturelle, ombres douces, matière FDM mate et échelle de petit objet de comptoir. Réserver le graphisme QR exact à la composition depuis le fichier fourni.

Le code QR final est composé depuis le PNG/SVG généré par le site. Vérifier le décodage après composition, car un générateur peut modifier ses modules.

## Prompt 3 — Packshot, 1:1

> À partir de la référence approuvée du produit MustDesign3D, créer un packshot sur fond ivoire uniforme avec une ombre de contact douce. Respecter la forme, les dimensions relatives, les couleurs et les graphismes de la référence. Cadrer l’objet entier avec une marge régulière et une lumière qui révèle sa matière mate.

## Prompt 4 — Détail d’impression, 4:3

> Montrer un détail du prototype de référence, avec une focale proche et un éclairage doux révélant les lettres en relief, le bord ou l’assemblage. Garder une profondeur de champ permettant de lire le détail utile. Préserver le matériau, les couleurs et la géométrie du produit de référence.

## Acceptation d’un média

- Correspondance du contour, des trous, du support, du nombre de composants et de l’épaisseur.
- Texte français/arabe vérifié visuellement et repris depuis le graphisme original si nécessaire.
- Palette compatible avec les filaments et cohérente entre les trois vues.
- Échelle cohérente avec les accessoires.
- QR vérifié après génération/composition.
- Type de média déclaré dans le catalogue.
- Fichiers source conservés et export web optimisé.

## Suggestions pour la prochaine séance photo réelle

Photographier chaque prototype sur le même fond neutre, puis dans son contexte d’usage. Ajouter une règle ou un objet d’échelle sur une vue technique. Capturer l’anneau du porte-clés, la stabilité d’un support et la lecture du QR. Remplacer les concepts de la fiche par les photos dont le prototype et les couleurs correspondent exactement.
```

## Fichier prompts/handoff/README.md

```markdown
# Paquet de reprise MustDesign3D

Ce dossier rassemble le contexte partageable avec un autre agent ou modèle. Le README reçu en pièce jointe a été lu comme référence en lecture seule.

## Les deux versions prêtes à transmettre

- [Version Gemini](GEMINI_MASTER.md), contexte de projet, plan de travail et instructions pour le code et les images.
- [Version Copilot](COPILOT_MASTER.md), contexte de projet et déroulé orienté fichiers, terminal et vérification dans VS Code.

Chaque version inclut le prompt maître commun et peut être utilisée seule avec le code du projet ou le snapshot.

## Contexte complémentaire

- [Prompt maître commun](MASTER_PROJECT.md), décisions et suggestions classées P0/P1/P2.
- [Brief photo](PHOTO_PROMPTS.md), deux essais pilotes et prompts réutilisables.
- [Source du projet](PROJECT_SOURCE.md), export textuel des sources et manifeste des fichiers.
- [Plan de refonte détaillé](../05-plan-refonte-niches-et-photos.md).

## Préparer un autre agent

1. Choisir GEMINI_MASTER.md ou COPILOT_MASTER.md.
2. Donner le dossier du projet à l’agent ou joindre PROJECT_SOURCE.md.
3. Pour un travail photo, joindre PHOTO_PROMPTS.md et l’image du modèle ou du prototype approuvé.
4. Demander un lot P0 ciblé puis vérifier les sorties.
5. Récupérer le code et les médias, lancer les contrôles et régénérer l’export.

## Actualiser l’export

Depuis la racine, exécuter npm run handoff. Le script exporte les sources textuelles autorisées, le lockfile, les SCAD et les guides de reprise. Les assets binaires sont listés avec SHA256 et restent à transférer séparément pour une reprise complète.

Les variables d’environnement, credentials, node_modules, .next, journaux et données de navigateur sont exclus. Examiner le fichier avant de le joindre à un service externe.

Le script de recette est inclus comme source. Les PDF/DOCX reçus se trouvent hors du projet et peuvent être joints séparément pour un nouveau travail de recherche. Le contexte maître contient les décisions nécessaires à une reprise du code.

## État de cette reprise

Le catalogue est structuré en neuf concepts et trois collections. Les références sur devis sont distinguées des prix fixes. Les couleurs de départ sont bleu, noir, blanc et rouge. Les vues techniques sont séparées des médias commerciaux et le QR est généré depuis le lien HTTPS. Les anciens modèles restent consultables dans /modeles.

Les nouvelles photos de concept restent à produire avec le générateur choisi. La forme finale des nouveaux produits et les fichiers de fabrication associés restent à valider. Le code est livré pour une démonstration locale.
```

## Fichier prompts/recherche/01-sources-et-selection.md

```markdown
# Recherche et sélection MustDesign3D

Relevé du 10 novembre 2026, obtenu avec Search Service et consultation HTTP des pages publiques. Les recommandations de cette note sont des choix de projet.

## 1. Résultats et couverture

| Référence | Observation vérifiée | Application à MustDesign3D |
| --- | --- | --- |
| To7fa | Catalogue par catégories, recherche, options de personnalisation et chemin de demande sur mesure | Navigation catalogue, filtres et distinction produit/projet |
| 3DGIFI, fiche pixel | Kit annoncé à 249 MAD, grille 24 × 24, 1 000 pièces, cinq couleurs et recommandations associées | Fiche explicative et propositions complémentaires |
| SliSearch | Moteur de découverte qui renvoie aux marketplaces d’origine et décrit les licences | Recherche interne de modèles et preuves à vérifier chez le créateur |

Les pages To7fa donnent des décomptes différents selon le relevé. L’accueil consulté indiquait 227 produits, une version du catalogue indexée par Search Service indiquait 228. Le sitemap et les liens du HTML récupérés directement ont tous deux donné 227 URLs françaises distinctes. L’inventaire joint contient ces 227 liens, sans visite individuelle de toutes les fiches. [Accueil To7fa](https://to7fa.ma/) · [Catalogue](https://to7fa.ma/produits) · [Sitemap](https://to7fa.ma/sitemap.xml)

Le kit pixel demande de nombreuses pièces et annonce cinq couleurs. Une création MustDesign3D inspirée de ce besoin prendrait la forme d’une plaque décorative originale, de deux à quatre couleurs, à tester séparément. L’adéquation du kit complet à la production A1 reste à étudier. [Fiche 3DGIFI](https://3dgifi.ma/product/pixel-emoji-collection/)

La page générale /en/models/ était inaccessible avec Search Service pendant cette recherche. Des résultats ciblés et le guide des licences étaient lisibles. Le guide affichait 1 169 822 modèles provenant de 23 marketplaces au moment de la consultation. La couverture du relevé SliSearch est donc un échantillon ciblé. [Guide SliSearch](https://slisearch.com/en/docs/licences)

## 2. Catalogue de démarrage recommandé

Les noms ci-dessous sont des pistes MustDesign3D. Les six slugs existants sont conservés. La complexité et les couleurs sont des objectifs de conception à vérifier sur prototype.

| Priorité | Produit | Objectif client | Conception visée | Prix démo existant |
| --- | --- | --- | --- | --- |
| 1 | Porte-clés prénom | Cadeau nominatif | Plat, arabe/latin, deux à quatre couleurs | 49 MAD |
| 2 | Plaque de bureau | Identifier un espace de travail | Texte en relief et socle simple | 129 MAD |
| 3 | Support QR | Présenter un lien sur un comptoir | Contraste élevé et socle stable | 149 MAD |
| 4 | Plaque de porte | Nommer une chambre ou un atelier | Plaque plate, deux couleurs | 99 MAD |
| 5 | Décor de ville | Décorer avec une identité locale | Silhouette originale en relief | 199 MAD |
| 6 | Présentoir logo | Présenter une entreprise | Logo fourni avec autorisation et socle | 199 MAD |
| À étudier | Range-câbles | Organiser un bureau | Petit clip ou support monobloc | À chiffrer |
| À étudier | Support téléphone | Poser un téléphone | Géométrie stable et peu de matière | À chiffrer |
| À étudier | Marque-page personnalisé | Petit cadeau de lecture | Plaque fine et détails lisibles | À chiffrer |
| Expérimental | Plaque pixel | Créer une déco graphique | Motif original et quatre couleurs maximum | À chiffrer |

Les montants démo proviennent de lib/products.ts. Ils nécessitent une validation économique et restent modifiables. Chaque piste vise un besoin observé dans les familles des références. Les temps et marges MustDesign3D restent à mesurer.

## 3. Sélectionner avant d’élargir

Pour chacun des dix concepts, noter difficulté /10, dimensions, nombre de couleurs, supports, capacité par plateau, temps de personnalisation, droits et besoin client. Retenir les trois vedettes lorsque l’A1 peut les produire de manière répétable.

Au slicing, relever le poids objet, la purge, le temps total, l’amortissement de préparation et les consommables. Calculer le coût complet par pièce, la marge et le gain par heure de machine. Indiquer les valeurs inconnues explicitement.

Le kit pixel complet, les lampes, les pièces exposées à la chaleur et les objets à contact alimentaire nécessitent une étude dédiée avant d’élargir le catalogue.

## 4. Recherches à poursuivre

- Maroc, utiliser les expressions « porte-clés prénom arabe », « plaque bureau personnalisée », « support QR commerce » et comparer les offres réellement accessibles.
- Modèles, utiliser les requêtes ciblées et les filtres commerciaux du registre modèles.
- Éviter de conclure à une forte demande à partir d’une seule fiche ou du nombre de téléchargements.
- Photographier un prototype, faire tester sa lisibilité et sa solidité, puis confirmer le prix avec les coûts locaux.

## 5. Livrable de recherche suivant

Compléter dix fiches internes avec besoin, lien source, créateur, preuves de droits, contraintes A1, photos originales et coût vérifié. Les fichiers autorisés restent dans un stockage de production privé. Les images publiées possèdent leur propre preuve d’utilisation.
```

## Fichier prompts/recherche/02-inventaire-to7fa.md

```markdown
# Inventaire des références produit To7fa

Relevé direct du 10 novembre 2026. **227 URLs françaises distinctes** sont présentes dans le sitemap public et dans le catalogue HTML récupéré. Les variantes linguistiques ont été écartées. Le compteur de la version indexée du catalogue peut différer.

Ce tableau conserve les liens pour la veille et l’étude des familles de produits. Les fiches individuelles restent à consulter pour leur prix, leurs variantes et leur disponibilité. Les fichiers 3D, médias et autorisations associés restent à identifier.

Sources du relevé, [sitemap public](https://to7fa.ma/sitemap.xml) et [catalogue](https://to7fa.ma/produits).

| Référence de veille | Adresse |
| --- | --- |
| T7-001 | [Fiche produit](https://to7fa.ma/produits/abat-jour-galbe) |
| T7-002 | [Fiche produit](https://to7fa.ma/produits/abat-jour-montgolfiere) |
| T7-003 | [Fiche produit](https://to7fa.ma/produits/abat-jour-ondule) |
| T7-004 | [Fiche produit](https://to7fa.ma/produits/abat-jour-vague) |
| T7-005 | [Fiche produit](https://to7fa.ma/produits/abat-jour-vannerie) |
| T7-006 | [Fiche produit](https://to7fa.ma/produits/anneau-a-balle-pour-chat) |
| T7-007 | [Fiche produit](https://to7fa.ma/produits/boite-a-bijoux-sardines) |
| T7-008 | [Fiche produit](https://to7fa.ma/produits/boite-a-mouchoirs-silhouette) |
| T7-009 | [Fiche produit](https://to7fa.ma/produits/boite-cadeau-happy-birthday) |
| T7-010 | [Fiche produit](https://to7fa.ma/produits/boite-de-rangement-moderne) |
| T7-011 | [Fiche produit](https://to7fa.ma/produits/boite-rainuree-japandi) |
| T7-012 | [Fiche produit](https://to7fa.ma/produits/boucles-attrape-reves) |
| T7-013 | [Fiche produit](https://to7fa.ma/produits/boucles-c-ur-tresse) |
| T7-014 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-avion-origami) |
| T7-015 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-colibri-aerien) |
| T7-016 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-coquillage) |
| T7-017 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-c-ur-infini) |
| T7-018 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-curseur) |
| T7-019 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-dentelle-blanche) |
| T7-020 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-douces-pattes) |
| T7-021 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-epure) |
| T7-022 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-flocon-etoile) |
| T7-023 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-goutte-vegetale) |
| T7-024 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-initiale-personnalisee) |
| T7-025 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-lignes-epure) |
| T7-026 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-mandala) |
| T7-027 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-mandala-labyrinthe) |
| T7-028 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-n-ud-celtique) |
| T7-029 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-papillon) |
| T7-030 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-prenom) |
| T7-031 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-rose-delicate) |
| T7-032 | [Fiche produit](https://to7fa.ma/produits/boucles-d-oreilles-silhouette-epure) |
| T7-033 | [Fiche produit](https://to7fa.ma/produits/boucles-fleur-de-cerisier) |
| T7-034 | [Fiche produit](https://to7fa.ma/produits/boucles-goutte-ciselee) |
| T7-035 | [Fiche produit](https://to7fa.ma/produits/boucles-mandala-azur) |
| T7-036 | [Fiche produit](https://to7fa.ma/produits/boucles-paquerette-tressee) |
| T7-037 | [Fiche produit](https://to7fa.ma/produits/boucles-pendantes-cascade-vegetale) |
| T7-038 | [Fiche produit](https://to7fa.ma/produits/boucles-sculpturales-epure) |
| T7-039 | [Fiche produit](https://to7fa.ma/produits/boucles-silhouette-feline) |
| T7-040 | [Fiche produit](https://to7fa.ma/produits/cache-pot-cannele-japandi) |
| T7-041 | [Fiche produit](https://to7fa.ma/produits/cache-pot-cannele-ondine) |
| T7-042 | [Fiche produit](https://to7fa.ma/produits/cache-pot-cannele-retro) |
| T7-043 | [Fiche produit](https://to7fa.ma/produits/cache-pot-cube-bulles) |
| T7-044 | [Fiche produit](https://to7fa.ma/produits/cache-pot-douce-lecture) |
| T7-045 | [Fiche produit](https://to7fa.ma/produits/cache-pot-ecailles-sculptees) |
| T7-046 | [Fiche produit](https://to7fa.ma/produits/cache-pot-feuillage-monstera) |
| T7-047 | [Fiche produit](https://to7fa.ma/produits/cache-pot-geometrique-vori) |
| T7-048 | [Fiche produit](https://to7fa.ma/produits/cache-pot-lune-socle) |
| T7-049 | [Fiche produit](https://to7fa.ma/produits/cache-pot-papier-froisse) |
| T7-050 | [Fiche produit](https://to7fa.ma/produits/cache-pot-petit-bonhomme) |
| T7-051 | [Fiche produit](https://to7fa.ma/produits/cache-pot-polygonal) |
| T7-052 | [Fiche produit](https://to7fa.ma/produits/cache-pot-relief-ecu) |
| T7-053 | [Fiche produit](https://to7fa.ma/produits/cache-pot-silhouette-feline) |
| T7-054 | [Fiche produit](https://to7fa.ma/produits/cache-pot-sur-pieds) |
| T7-055 | [Fiche produit](https://to7fa.ma/produits/cache-pot-torsade-claudia) |
| T7-056 | [Fiche produit](https://to7fa.ma/produits/cadres-happy-birthday) |
| T7-057 | [Fiche produit](https://to7fa.ma/produits/cake-topper-happy-birthday) |
| T7-058 | [Fiche produit](https://to7fa.ma/produits/cake-topper-happy-birthday-elegant) |
| T7-059 | [Fiche produit](https://to7fa.ma/produits/cake-topper-prenom-et-age) |
| T7-060 | [Fiche produit](https://to7fa.ma/produits/coupe-graphique-ajouree) |
| T7-061 | [Fiche produit](https://to7fa.ma/produits/coupelle-aperitive-duo) |
| T7-062 | [Fiche produit](https://to7fa.ma/produits/couronne-d-anniversaire) |
| T7-063 | [Fiche produit](https://to7fa.ma/produits/couronne-sculpturale-japandi) |
| T7-064 | [Fiche produit](https://to7fa.ma/produits/coussin-pour-telephone) |
| T7-065 | [Fiche produit](https://to7fa.ma/produits/crochet-a-casque) |
| T7-066 | [Fiche produit](https://to7fa.ma/produits/crochet-a-serviette-autobloquant) |
| T7-067 | [Fiche produit](https://to7fa.ma/produits/crochet-mural-minimaliste) |
| T7-068 | [Fiche produit](https://to7fa.ma/produits/c-ur-a-la-rose-eternelle) |
| T7-069 | [Fiche produit](https://to7fa.ma/produits/deco-de-table-happy-birthday) |
| T7-070 | [Fiche produit](https://to7fa.ma/produits/distributeur-de-friandises-pour-chat) |
| T7-071 | [Fiche produit](https://to7fa.ma/produits/ecrin-porte-encens-zen) |
| T7-072 | [Fiche produit](https://to7fa.ma/produits/embout-crayon-prenom-debout) |
| T7-073 | [Fiche produit](https://to7fa.ma/produits/embout-prenom-pour-crayon-paille) |
| T7-074 | [Fiche produit](https://to7fa.ma/produits/etagere-a-tasses-compacte) |
| T7-075 | [Fiche produit](https://to7fa.ma/produits/etiquette-bagage-personnalisee) |
| T7-076 | [Fiche produit](https://to7fa.ma/produits/etui-a-briquet-ecailles) |
| T7-077 | [Fiche produit](https://to7fa.ma/produits/etui-briquet-alveole) |
| T7-078 | [Fiche produit](https://to7fa.ma/produits/etui-briquet-graphique) |
| T7-079 | [Fiche produit](https://to7fa.ma/produits/etui-briquet-lignes-fluides) |
| T7-080 | [Fiche produit](https://to7fa.ma/produits/etui-capsule-pour-briquet) |
| T7-081 | [Fiche produit](https://to7fa.ma/produits/etui-nomade-pour-mini-briquet) |
| T7-082 | [Fiche produit](https://to7fa.ma/produits/etui-texture-mini-briquet) |
| T7-083 | [Fiche produit](https://to7fa.ma/produits/figurines-anniversaire-en-chiffres) |
| T7-084 | [Fiche produit](https://to7fa.ma/produits/flacon-enchante-d-apothicaire) |
| T7-085 | [Fiche produit](https://to7fa.ma/produits/fourreau-porte-cles-pour-briquet) |
| T7-086 | [Fiche produit](https://to7fa.ma/produits/gamelle-a-eau-autoremplissante) |
| T7-087 | [Fiche produit](https://to7fa.ma/produits/gourde-et-gamelle-de-balade) |
| T7-088 | [Fiche produit](https://to7fa.ma/produits/initiales-de-couple-personnalisees) |
| T7-089 | [Fiche produit](https://to7fa.ma/produits/initiales-pour-dragees) |
| T7-090 | [Fiche produit](https://to7fa.ma/produits/jardiniere-pluie-zen-minerale) |
| T7-091 | [Fiche produit](https://to7fa.ma/produits/jouets-pour-chat-lot) |
| T7-092 | [Fiche produit](https://to7fa.ma/produits/jouets-pour-chat-v2-lot) |
| T7-093 | [Fiche produit](https://to7fa.ma/produits/lampe-champignon-cotelee) |
| T7-094 | [Fiche produit](https://to7fa.ma/produits/lampe-cubes-empiles) |
| T7-095 | [Fiche produit](https://to7fa.ma/produits/lampe-cumulis) |
| T7-096 | [Fiche produit](https://to7fa.ma/produits/lampe-d-ambiance-croissant) |
| T7-097 | [Fiche produit](https://to7fa.ma/produits/lampe-flamme-de-lotus) |
| T7-098 | [Fiche produit](https://to7fa.ma/produits/lampe-fusee-odyssee) |
| T7-099 | [Fiche produit](https://to7fa.ma/produits/lampe-fusee-retro) |
| T7-100 | [Fiche produit](https://to7fa.ma/produits/lampe-la-vague) |
| T7-101 | [Fiche produit](https://to7fa.ma/produits/lampe-loopy-timide) |
| T7-102 | [Fiche produit](https://to7fa.ma/produits/lampe-lune) |
| T7-103 | [Fiche produit](https://to7fa.ma/produits/lampe-ondine) |
| T7-104 | [Fiche produit](https://to7fa.ma/produits/lampe-organique-astrale) |
| T7-105 | [Fiche produit](https://to7fa.ma/produits/lampe-pieuvre) |
| T7-106 | [Fiche produit](https://to7fa.ma/produits/lampe-prisme) |
| T7-107 | [Fiche produit](https://to7fa.ma/produits/lampe-sculpturale-sharon) |
| T7-108 | [Fiche produit](https://to7fa.ma/produits/lampe-spirale-rayee) |
| T7-109 | [Fiche produit](https://to7fa.ma/produits/lampe-trepied) |
| T7-110 | [Fiche produit](https://to7fa.ma/produits/le-petit-barista) |
| T7-111 | [Fiche produit](https://to7fa.ma/produits/lettre-de-naissance-mensurations) |
| T7-112 | [Fiche produit](https://to7fa.ma/produits/lettre-de-naissance-personnalisee) |
| T7-113 | [Fiche produit](https://to7fa.ma/produits/lettres-prenom-chambre-bebe) |
| T7-114 | [Fiche produit](https://to7fa.ma/produits/lune-sur-socle-ondule) |
| T7-115 | [Fiche produit](https://to7fa.ma/produits/mangeoire-a-oiseaux-minimaliste) |
| T7-116 | [Fiche produit](https://to7fa.ma/produits/mangeoire-a-oiseaux-moderne) |
| T7-117 | [Fiche produit](https://to7fa.ma/produits/marque-page-fermeture-eclair) |
| T7-118 | [Fiche produit](https://to7fa.ma/produits/marque-page-feuilles-de-palmier) |
| T7-119 | [Fiche produit](https://to7fa.ma/produits/marque-page-japon) |
| T7-120 | [Fiche produit](https://to7fa.ma/produits/marque-page-la-grande-vague) |
| T7-121 | [Fiche produit](https://to7fa.ma/produits/marque-page-papillon-monarque) |
| T7-122 | [Fiche produit](https://to7fa.ma/produits/medaille-pour-animal) |
| T7-123 | [Fiche produit](https://to7fa.ma/produits/mini-support-de-poche) |
| T7-124 | [Fiche produit](https://to7fa.ma/produits/monogramme-prenom) |
| T7-125 | [Fiche produit](https://to7fa.ma/produits/organisateur-cotele-pour-telecommandes) |
| T7-126 | [Fiche produit](https://to7fa.ma/produits/organisateur-d-evier-auto-egouttant) |
| T7-127 | [Fiche produit](https://to7fa.ma/produits/organiseur-de-chevet) |
| T7-128 | [Fiche produit](https://to7fa.ma/produits/organiseur-mural-et-porte-cles) |
| T7-129 | [Fiche produit](https://to7fa.ma/produits/organiseur-prenom-c-ur) |
| T7-130 | [Fiche produit](https://to7fa.ma/produits/panier-empilable-ajoure) |
| T7-131 | [Fiche produit](https://to7fa.ma/produits/patere-murale-epure) |
| T7-132 | [Fiche produit](https://to7fa.ma/produits/perles-fleurs-lettres) |
| T7-133 | [Fiche produit](https://to7fa.ma/produits/perles-lettres-personnalisees) |
| T7-134 | [Fiche produit](https://to7fa.ma/produits/perles-oursons-lettres) |
| T7-135 | [Fiche produit](https://to7fa.ma/produits/petite-lampe-evasee) |
| T7-136 | [Fiche produit](https://to7fa.ma/produits/pince-a-sachet-hermetique) |
| T7-137 | [Fiche produit](https://to7fa.ma/produits/plaque-d-adresse-moderne) |
| T7-138 | [Fiche produit](https://to7fa.ma/produits/plaque-de-porte-classique) |
| T7-139 | [Fiche produit](https://to7fa.ma/produits/poire-a-friandises-pour-chat) |
| T7-140 | [Fiche produit](https://to7fa.ma/produits/porte-baume-a-levres-fleuri) |
| T7-141 | [Fiche produit](https://to7fa.ma/produits/porte-brosses-a-dents-cotele) |
| T7-142 | [Fiche produit](https://to7fa.ma/produits/porte-cles-disque-de-fonte) |
| T7-143 | [Fiche produit](https://to7fa.ma/produits/porte-cles-initiale-et-prenom) |
| T7-144 | [Fiche produit](https://to7fa.ma/produits/porte-cles-lettre-d-amour) |
| T7-145 | [Fiche produit](https://to7fa.ma/produits/porte-cles-logo-personnalise) |
| T7-146 | [Fiche produit](https://to7fa.ma/produits/porte-cles-maillot-de-foot) |
| T7-147 | [Fiche produit](https://to7fa.ma/produits/porte-cles-plaque-europeenne) |
| T7-148 | [Fiche produit](https://to7fa.ma/produits/porte-cles-plaque-immatriculation) |
| T7-149 | [Fiche produit](https://to7fa.ma/produits/porte-cles-prenom) |
| T7-150 | [Fiche produit](https://to7fa.ma/produits/porte-cles-prenom-a-bordure) |
| T7-151 | [Fiche produit](https://to7fa.ma/produits/porte-cles-prenom-bulle) |
| T7-152 | [Fiche produit](https://to7fa.ma/produits/porte-cles-prenom-double-contour) |
| T7-153 | [Fiche produit](https://to7fa.ma/produits/porte-cles-prenom-en-relief) |
| T7-154 | [Fiche produit](https://to7fa.ma/produits/porte-cles-prenom-et-c-ur) |
| T7-155 | [Fiche produit](https://to7fa.ma/produits/porte-cles-prenom-gonfle-3d) |
| T7-156 | [Fiche produit](https://to7fa.ma/produits/porte-cles-prenom-marguerite) |
| T7-157 | [Fiche produit](https://to7fa.ma/produits/porte-cles-touche-typographique) |
| T7-158 | [Fiche produit](https://to7fa.ma/produits/porte-crayons-trio-prenom) |
| T7-159 | [Fiche produit](https://to7fa.ma/produits/porte-encens-cascade-celeste) |
| T7-160 | [Fiche produit](https://to7fa.ma/produits/porte-encens-cascade-epuree) |
| T7-161 | [Fiche produit](https://to7fa.ma/produits/porte-encens-cascade-zen) |
| T7-162 | [Fiche produit](https://to7fa.ma/produits/porte-encens-cheminee-retro) |
| T7-163 | [Fiche produit](https://to7fa.ma/produits/porte-encens-chevalier-noir) |
| T7-164 | [Fiche produit](https://to7fa.ma/produits/porte-encens-coffret-epure) |
| T7-165 | [Fiche produit](https://to7fa.ma/produits/porte-encens-coussin-organique) |
| T7-166 | [Fiche produit](https://to7fa.ma/produits/porte-encens-fleur-de-lotus) |
| T7-167 | [Fiche produit](https://to7fa.ma/produits/porte-encens-fleur-marguerite) |
| T7-168 | [Fiche produit](https://to7fa.ma/produits/porte-encens-le-pecheur-zen) |
| T7-169 | [Fiche produit](https://to7fa.ma/produits/porte-encens-le-voyageur-cosmique) |
| T7-170 | [Fiche produit](https://to7fa.ma/produits/porte-encens-lotus-zen) |
| T7-171 | [Fiche produit](https://to7fa.ma/produits/porte-encens-onde-pure) |
| T7-172 | [Fiche produit](https://to7fa.ma/produits/porte-encens-onde-sereine) |
| T7-173 | [Fiche produit](https://to7fa.ma/produits/porte-encens-ovale-epure) |
| T7-174 | [Fiche produit](https://to7fa.ma/produits/porte-encens-rosace-mandala) |
| T7-175 | [Fiche produit](https://to7fa.ma/produits/porte-encens-sillage-epure) |
| T7-176 | [Fiche produit](https://to7fa.ma/produits/porte-encens-sillage-lineaire) |
| T7-177 | [Fiche produit](https://to7fa.ma/produits/porte-encens-tout-en-un-epure) |
| T7-178 | [Fiche produit](https://to7fa.ma/produits/porte-encens-vertical-epure) |
| T7-179 | [Fiche produit](https://to7fa.ma/produits/porte-essuie-tout-japandi) |
| T7-180 | [Fiche produit](https://to7fa.ma/produits/porte-gamelle-personnalise) |
| T7-181 | [Fiche produit](https://to7fa.ma/produits/porte-savon-cascade-epure) |
| T7-182 | [Fiche produit](https://to7fa.ma/produits/porte-serviettes-feuille-monstera) |
| T7-183 | [Fiche produit](https://to7fa.ma/produits/pot-a-crayons-cotele) |
| T7-184 | [Fiche produit](https://to7fa.ma/produits/pot-a-crayons-t-rex) |
| T7-185 | [Fiche produit](https://to7fa.ma/produits/pot-a-ustensiles-de-cuisine) |
| T7-186 | [Fiche produit](https://to7fa.ma/produits/pot-epure-avec-coupelle) |
| T7-187 | [Fiche produit](https://to7fa.ma/produits/pot-mains-en-c-ur) |
| T7-188 | [Fiche produit](https://to7fa.ma/produits/prenom-calligraphie-arabe) |
| T7-189 | [Fiche produit](https://to7fa.ma/produits/prenom-de-bebe-sur-socle) |
| T7-190 | [Fiche produit](https://to7fa.ma/produits/prenom-decoratif) |
| T7-191 | [Fiche produit](https://to7fa.ma/produits/prenom-lettres-bulles) |
| T7-192 | [Fiche produit](https://to7fa.ma/produits/prenoms-pour-dragees) |
| T7-193 | [Fiche produit](https://to7fa.ma/produits/prenom-sur-crayon) |
| T7-194 | [Fiche produit](https://to7fa.ma/produits/presentoir-avis-nfc-qr) |
| T7-195 | [Fiche produit](https://to7fa.ma/produits/range-cables-usb) |
| T7-196 | [Fiche produit](https://to7fa.ma/produits/range-chaussures-a-languette) |
| T7-197 | [Fiche produit](https://to7fa.ma/produits/socle-de-gamelle-epure) |
| T7-198 | [Fiche produit](https://to7fa.ma/produits/sous-verres-alveoles) |
| T7-199 | [Fiche produit](https://to7fa.ma/produits/sous-verres-feuilles-de-monstera) |
| T7-200 | [Fiche produit](https://to7fa.ma/produits/station-de-bouturage-epure) |
| T7-201 | [Fiche produit](https://to7fa.ma/produits/statuette-feline-c-ur) |
| T7-202 | [Fiche produit](https://to7fa.ma/produits/support-dentifrice-brosses-brique) |
| T7-203 | [Fiche produit](https://to7fa.ma/produits/support-d-eponge-pour-robinet) |
| T7-204 | [Fiche produit](https://to7fa.ma/produits/support-egouttoir-japandi) |
| T7-205 | [Fiche produit](https://to7fa.ma/produits/support-pese-personne-arche) |
| T7-206 | [Fiche produit](https://to7fa.ma/produits/support-telephone-bicolore) |
| T7-207 | [Fiche produit](https://to7fa.ma/produits/support-telephone-essentiel) |
| T7-208 | [Fiche produit](https://to7fa.ma/produits/support-telephone-galbe) |
| T7-209 | [Fiche produit](https://to7fa.ma/produits/support-telephone-inclinable) |
| T7-210 | [Fiche produit](https://to7fa.ma/produits/suspension-ondulee) |
| T7-211 | [Fiche produit](https://to7fa.ma/produits/tient-page-de-lecture) |
| T7-212 | [Fiche produit](https://to7fa.ma/produits/topper-chiffre-pour-gateau) |
| T7-213 | [Fiche produit](https://to7fa.ma/produits/vase-baluchon-plisse) |
| T7-214 | [Fiche produit](https://to7fa.ma/produits/vase-boite-c-ur) |
| T7-215 | [Fiche produit](https://to7fa.ma/produits/vase-cotele-japandi) |
| T7-216 | [Fiche produit](https://to7fa.ma/produits/vase-c-ur) |
| T7-217 | [Fiche produit](https://to7fa.ma/produits/vase-japandi-shizu) |
| T7-218 | [Fiche produit](https://to7fa.ma/produits/vase-minimal) |
| T7-219 | [Fiche produit](https://to7fa.ma/produits/vase-sculptural-croissant-lunaire) |
| T7-220 | [Fiche produit](https://to7fa.ma/produits/vase-sculptural-felicia) |
| T7-221 | [Fiche produit](https://to7fa.ma/produits/vase-sculptural-l-audacieux) |
| T7-222 | [Fiche produit](https://to7fa.ma/produits/vases-japandi) |
| T7-223 | [Fiche produit](https://to7fa.ma/produits/vase-soliflore-facette) |
| T7-224 | [Fiche produit](https://to7fa.ma/produits/vase-spirale) |
| T7-225 | [Fiche produit](https://to7fa.ma/produits/vases-torus-entrelaces) |
| T7-226 | [Fiche produit](https://to7fa.ma/produits/vase-vanta) |
| T7-227 | [Fiche produit](https://to7fa.ma/produits/voronoi-modern-design-incense-holder) |

## Suite du travail

Consulter les fiches pertinentes pour les dix concepts de démarrage. Pour chaque produit retenu, créer une proposition MustDesign3D avec sa propre conception ou une source de modèle autorisée, puis appliquer le registre de droits et la validation A1.
```

## Fichier prompts/recherche/03-modeles-et-import.md

````markdown
# Modèles, licences et import

## 1. Registre initial

Relevé du 10 novembre 2026. « Résultat indexé » signifie que Search Service a exposé une fiche ou un extrait. Tous les candidats gardent le statut needs_review tant que la marketplace d’origine, la licence et le fichier n’ont pas été contrôlés. Ce registre recense des pistes et des liens.

| ID interne | Piste | Information disponible | Source |
| --- | --- | --- | --- |
| model-name-keychain | Porte-clés prénom paramétrique | Résultat indexé, auteur C4UStudio, fichier SCAD, CC BY-SA annoncé par l’agrégateur. La lecture directe a expiré | [Fiche SliSearch](https://slisearch.com/en/models/a2835fdd-4161-4afc-9e40-ca4f725e8437) |
| model-two-line | Porte-clés à deux lignes | Usage commercial mentionné dans le résultat indexé, détails chez le créateur à confirmer | [Fiche SliSearch](https://slisearch.com/en/models/e453cb73-515b-4ccc-90ed-964e156315b5) |
| model-cable-clip | Clip de câble | CC0 annoncé dans le résultat indexé, fichier et source à contrôler | [Fiche SliSearch](https://slisearch.com/en/models/a8c75b85-e141-43cd-9e0b-ffe699ddbbfe) |
| model-usb-holder | Support de câbles modulaire | CC0 annoncé dans le résultat indexé, géométrie et source à contrôler | [Fiche SliSearch](https://slisearch.com/en/models/0f518b80-01b6-4a13-8826-679aba259493) |
| model-room-signs | Plaques de pièces | Résultat relié à Printables, conditions commerciales à confirmer | [Fiche SliSearch](https://slisearch.com/en/models/e5353a97-544c-44a8-8fc0-9e9856c93ed7) |
| model-standard-keychain | Porte-clés personnalisable | Licence marketplace standard annoncée, permissions à contrôler | [Fiche SliSearch](https://slisearch.com/en/models/dba7c166-9720-435a-81b2-313c1e181b22) |
| model-business-card | Carte de visite imprimable | Usage personnel et non commercial annoncé dans le résultat, réserver à l’étude | [Fiche SliSearch](https://slisearch.com/en/models/dc34943c-c227-4573-8a35-34474ffdf247) |
| model-qr-generator | Générateur QR | Restriction non commerciale annoncée dans le résultat, réserver à l’étude | [Fiche SliSearch](https://slisearch.com/en/models/22660a2f-58c7-45d3-8453-0d69c1b6ce13) |

La piste plaque de bureau en 6e4d0130-1c44-4c2e-84b8-88a17f1f40b0 était indexée, mais la lecture directe a donné 404. La conserver uniquement dans le journal de recherche. [Adresse testée](https://slisearch.com/en/models/6e4d0130-1c44-4c2e-84b8-88a17f1f40b0)

Le filtre licence:commercial aide à trouver des candidats. La décision d’utilisation repose sur les conditions de la source originale et sur les droits des visuels séparément. [Documentation des licences](https://slisearch.com/en/docs/licences)

## 2. Requêtes de départ

Dans Search Service, effectuer des recherches ciblées, puis ouvrir les fiches qui répondent au besoin.

```text
site:slisearch.com/en/models/ "name keychain" "commercial"
site:slisearch.com/en/models/ "desk name" "license"
site:slisearch.com/en/models/ "QR stand" "commercial"
site:slisearch.com/en/models/ "cable" "CC0"
site:slisearch.com/en/models/ "door sign" "license"
```

Dans l’interface SliSearch, ajouter licence:commercial et privilégier un fichier paramétrique modifiable quand la personnalisation est nécessaire.

## 3. Constituer une bibliothèque utilisable

1. Choisir un concept dans le catalogue de démarrage.
2. Retrouver la page d’origine, le créateur et la version du modèle.
3. Lire les permissions pour les impressions commerciales, les modifications et la redistribution numérique. Identifier l’attribution requise.
4. Vérifier que les éléments tiers du modèle et les visuels ont leurs propres autorisations.
5. Conserver le lien et une preuve datée de licence ou d’achat dans le dossier interne du projet.
6. Télécharger le fichier depuis la marketplace autorisée lorsque les conditions le permettent.
7. Calculer SHA-256 sur le fichier, noter sa version et le conserver hors du dossier public du site.
8. Ouvrir le modèle dans Bambu Studio, vérifier sa géométrie et produire un prototype.
9. Photographier le résultat et rédiger une fiche MustDesign3D originale.
10. Faire passer la fiche en catalogue vendable après validation des droits, de la fabrication et du prix.

Les images de marketplace sont des références de recherche. La boutique utilise ses propres photos ou des médias dont le droit de publication est établi.

## 4. Import d’une liste de modèles

Prévoir un import administratif local avec prévisualisation. Une ligne contient au minimum sourceUrl, originalUrl si connu, creator, licenceLabel, observedAt, permissionCommercialPrint, permissionModify, permissionRedistribute, rightsEvidenceRef et reviewStatus.

- Les permissions valent true, false ou null selon les preuves.
- Dédupliquer par source et identifiant externe, puis rapprocher la source primaire. Une ressemblance de titre déclenche une vérification manuelle.
- Présenter les erreurs par ligne et conserver un bilan des lignes importées, mises à jour ou ignorées.
- Garder l’import en recherche jusqu’à validation explicite de chaque modèle.
- L’import traite des métadonnées. L’acquisition de fichiers reste une étape distincte.
- Une réimportation conserve les décisions, preuves et corrections manuelles. Une modification de licence crée une nouvelle observation et demande une revue.
- Un lien inaccessible garde son statut d’échec avec la date. Une reprise ne crée pas de doublon.

La source primaire est une URL externe, et le fichier détenu est un asset interne distinct. Cette séparation permet de suivre la provenance sans publier les fichiers de production.

## 5. État actuel

Aucun fichier de modèle ni média concurrent n’a été acquis pendant cette mise à jour documentaire. Les huit lignes du registre sont des pistes SliSearch, les 227 liens To7fa sont un inventaire public et la fiche 3DGIFI est une référence produit. La bibliothèque complète de SliSearch reste hors couverture du présent relevé.
````

## Fichier prompts/recherche/04-selection-et-integration.md

```markdown
# Modèles ajoutés à MustDesign3D

Reprise du 10 novembre 2026. Search Service a été utilisé pour consulter les trois références et rechercher la source primaire d’un candidat SliSearch.

## Intégration locale

La collection présente sept créations de démonstration, avec une page /modeles. Les six premières conservent leurs identifiants, leurs slugs et leurs prix indicatifs. La septième est une plaque pixel Zellige originale de 86 × 86 × 3,6 mm en trois couleurs. Son prix démo de 119 MAD est une hypothèse de présentation à confirmer par l’atelier.

Les sept sources OpenSCAD sont conservées dans production/. Les exports STL de configuration par défaut sont dans production/exports/. Les vues PNG du site ont été générées par OpenSCAD à partir de ces sources. Elles représentent les prototypes par défaut, et le configurateur conserve un aperçu 2D distinct pour les prénoms saisis.

Les assemblages, les graphies et les pièces séparées restent à contrôler dans Bambu Studio et sur une impression d’essai. Les prototypes QR/logo restent des gabarits. La plaque pixel est une décoration monobloc en relief.

## Recherche externe

- To7fa sert à étudier les familles, filtres et options du catalogue. Le relevé de 227 liens reste disponible dans 02-inventaire-to7fa.md. [Catalogue](https://to7fa.ma/produits)
- La fiche 3DGIFI sert de référence pour la présentation d’une création pixel. La plaque Zellige utilise une géométrie originale de trois couleurs et constitue une nouvelle piste MustDesign3D. [Fiche de référence](https://3dgifi.ma/product/pixel-emoji-collection/)
- Le candidat clip de câble repéré dans SliSearch a été relié à la fiche d’origine Cults de Nexo3d. La version indexée de cette fiche annonce CC0. La lecture directe et le téléchargement renvoient 403. Le fichier reste à acquérir chez le créateur et à vérifier avant intégration. [Fiche du créateur](https://cults3d.com/en/3d-model/gadget/universal-cable-clip-simple-cable-organizer-for-desk)

La page générale SliSearch reste inaccessible dans Search Service. Les découvertes ciblées apportent des pistes, et la bibliothèque externe conserve ses statuts de revue. [Guide de recherche et de licences](https://slisearch.com/en/docs/licences)

## Ajouter un prochain modèle

1. Acquérir le fichier depuis sa source autorisée et conserver les preuves d’utilisation.
2. Enregistrer l’auteur, la version et le SHA256 dans production/manifest.json.
3. Exporter en STL et contrôler les unités, dimensions et parties.
4. Générer une image dans public/models/ et déclarer sa provenance.
5. Ajouter le produit dans lib/catalogue.server.ts avec un id et un slug uniques, les dimensions connues et un schéma d’options adapté.
6. Garder status=demo jusqu’à validation du prototype et du prix.
7. Vérifier la fiche, la galerie, la recherche et le comportement du panier.
```

## Fichier railway.toml

```toml
[build]
buildCommand = "npm run build"

[deploy]
startCommand = "npm start"
healthcheckPath = "/"
healthcheckTimeout = 120
```

## Fichier scripts/export-handoff.mjs

```javascript
import fs from 'node:fs';
import path from 'node:path';
import crypto from 'node:crypto';
import { fileURLToPath } from 'node:url';

const root = fileURLToPath(new URL('../', import.meta.url));
const destination = 'prompts/handoff/PROJECT_SOURCE.md';
const textExtensions = new Set(['.ts', '.tsx', '.mjs', '.cjs', '.json', '.md', '.scad', '.toml', '.css']);
const rootFiles = ['package.json', 'package-lock.json', 'tsconfig.json', 'next.config.ts', 'postcss.config.mjs', 'railway.toml', '.gitignore', 'README.md', 'codex.md', '.goals/mustdesign3d-local/verification/smoke.cjs'];
const excluded = new Set(['node_modules', '.next', '.git', '.env', '.env.local', '.env.production', '.DS_Store']);
const language = { '.ts': 'typescript', '.tsx': 'tsx', '.mjs': 'javascript', '.cjs': 'javascript', '.json': 'json', '.css': 'css', '.scad': 'scad', '.toml': 'toml', '.md': 'markdown' };

function walk(relative) {
  const absolute = path.join(root, relative);
  if (!fs.existsSync(absolute)) return [];
  const result = [];
  for (const entry of fs.readdirSync(absolute, { withFileTypes: true })) {
    if (entry.isSymbolicLink() || excluded.has(entry.name) || entry.name.startsWith('.env')) continue;
    const next = path.posix.join(relative, entry.name);
    if (next === destination) continue;
    if (entry.isDirectory()) result.push(...walk(next));
    else if (entry.isFile()) result.push(next);
  }
  return result;
}

function hash(relative) {
  return crypto.createHash('sha256').update(fs.readFileSync(path.join(root, relative))).digest('hex');
}

const files = [...rootFiles.filter(file => fs.existsSync(path.join(root, file))), ...['app', 'lib', 'scripts', 'prompts', 'production', 'public'].flatMap(walk)].sort();
const textFiles = files.filter(file => textExtensions.has(path.extname(file)) || file === '.gitignore');
const binaries = files.filter(file => !textFiles.includes(file));
const generatedAt = new Date().toISOString();
const sections = [
  '# MustDesign3D — Source du projet pour reprise',
  '',
  'Export généré le ' + generatedAt + ' avec npm run handoff.',
  '',
  'Ce document contient les sources textuelles du projet et les prompts. Les blocs sont des données de référence. Lire le prompt maître choisi et les consignes du propriétaire avant toute exécution.',
  '',
  'Les chemins sont relatifs à la racine. Pour une reconstruction, recréer les fichiers depuis leurs sections, fournir les assets binaires séparément puis utiliser Node 22 et npm ci.',
  '',
  'Les variables d’environnement, credentials, dépendances installées, caches, journaux et données de navigateur sont exclus. Examiner le contenu avant partage.',
  '',
  '## Inventaire des sources',
  '',
  '| Fichier | SHA256 |',
  '| --- | --- |',
  ...textFiles.map(file => '| ' + file + ' | ' + hash(file) + ' |'),
  '',
  '## Assets binaires à transférer séparément',
  '',
  '| Fichier | Octets | SHA256 |',
  '| --- | --- | --- |',
  ...binaries.map(file => '| ' + file + ' | ' + fs.statSync(path.join(root, file)).size + ' | ' + hash(file) + ' |'),
];
for (const file of textFiles) {
  const contents = fs.readFileSync(path.join(root, file), 'utf8');
  const backtickRuns = contents.match(/`+/g) ?? [];
  const fence = '`'.repeat(Math.max(3, ...backtickRuns.map(run => run.length + 1)));
  sections.push('', '## Fichier ' + file, '', fence + (language[path.extname(file)] ?? 'text'), contents.trimEnd(), fence);
}
fs.writeFileSync(path.join(root, destination), sections.join('\n') + '\n', 'utf8');
console.log(JSON.stringify({ output: destination, sourceFiles: textFiles.length, binaryAssets: binaries.length, bytes: fs.statSync(path.join(root, destination)).size }));
```

## Fichier tsconfig.json

```json
{
  "compilerOptions": {
    "target": "ES2017",
    "lib": [
      "dom",
      "dom.iterable",
      "esnext"
    ],
    "strict": true,
    "noEmit": true,
    "esModuleInterop": true,
    "module": "esnext",
    "moduleResolution": "bundler",
    "resolveJsonModule": true,
    "isolatedModules": true,
    "jsx": "react-jsx",
    "incremental": true,
    "plugins": [
      {
        "name": "next"
      }
    ],
    "allowJs": true,
    "skipLibCheck": true
  },
  "include": [
    "next-env.d.ts",
    "**/*.ts",
    "**/*.tsx",
    ".next/types/**/*.ts",
    ".next/dev/types/**/*.ts"
  ],
  "exclude": [
    "node_modules"
  ]
}
```
