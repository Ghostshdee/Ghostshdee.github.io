# ghostshdee.github.io

**Dokay-гийн нүүр хуудас** — Жаргалсайхан Дөлгөөн (Дархан). AI автоматжуулалт,
вэб хөгжүүлэлт, контент, цахим урилга.

**Амьд хаяг:** https://ghostshdee.github.io/

Өмнөх тусдаа `dokay-portfolio` ба `dokay-ai-service` хоёр сайтыг нэг нүүр
хуудас болгон нэгтгэсэн (2026-09). Тэр хоёр repo одоо энэ хаяг руу чиглүүлэх
redirect хуудас болсон.

## Бүтэц

Ганц `index.html` (~1500 мөр). Бүх агуулга дээд талын **`CONFIG`** объектод.

Секцүүд: Hero → Тухай → Ур чадвар → Үйлчилгээ → Ажлын явц → Багц →
Ажлууд → FAQ → Холбоо барих → Footer.

- Дизайн: шохой ногоон `#C6F24E`, Oswald + Roboto Flex + Inter + JetBrains Mono
- GSAP 3.12 + ScrollTrigger + Lenis (pin-timeline hero, custom cursor)
- Tailwind Play CDN (`cdn.tailwindcss.com`)
- GSAP ирэхгүй / `prefers-reduced-motion` / далд таб үед бүх контент шууд
  харагдана (`html.anim` + 1400ms fallback, `.reveal-all`)

## Агуулга өөрчлөх

Зөвхөн `CONFIG`-оос. HTML/CSS-д гар хүрэх шаардлагагүй.

- **`CONFIG.seo`** — гарчиг, тайлбар, canonical, og зураг. `<head>` доторх
  мета тагийг ГАРААР давхар шинэчил (crawler JS ажиллуулдаггүй — доор үз).
- **`CONFIG.contact`** — утас, имэйл, Messenger/Facebook/Instagram.
- **`CONFIG.services` / `process` / `pricing` / `faq`** — тухайн секцийн агуулга.
- **`CONFIG.work.items`** — ажлын жагсаалт (доор).

## Ажил нэмэх

`CONFIG.work.items`-д нэг мөр нэмнэ:

```js
{
  title: 'Ажлын нэр', tag: 'ЦАХИМ УРИЛГА', year: '2026',
  desc:  'Товч тайлбар.',
  tech:  ['GSAP','RSVP'],
  img:   'assets/файл-нэр.jpg',   // 4:3 харьцаа, ~1200×900, JPG, 200–400 KB
  live:  'https://ghostshdee.github.io/repo-нэр/'   // хоосон + merged:true бол «нэгдсэн» тэмдэглэл
}
```

Зургаа `assets/` хавтсанд хийнэ. Хамгийн амар арга — амьд сайтын screenshot.

## SEO / Open Graph

`<head>` доторх `<title>`, `<meta>`, `og:*`, `twitter:*` тагуудыг **гараар**
шинэчилнэ — Facebook, Messenger зэрэг crawler JavaScript ажиллуулдаггүй тул
`CONFIG.seo`-оос автоматаар үүсгэх боломжгүй. Хоёуланг зэрэг тааруул.

**Хийх зүйл:** `assets/og.jpg` (1200×630) — одоохондоо байхгүй тул нийгмийн
сүлжээнд хуваалцахад зургийн урьдчилсан харагдац гарахгүй.

## JSON-LD

`injectSchema()` нь ажиллах үед `<head>`-д нэг `@graph` нэмнэ:
`Person` + `ProfessionalService` + `FAQPage` + `ItemList` — бүгд `CONFIG`-оос.
