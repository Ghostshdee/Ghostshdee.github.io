# ghostshdee.github.io

Dokay-гийн нүүр хуудас — хийгдсэн ажлуудын жагсаалт.

**Амьд хаяг:** https://ghostshdee.github.io/

Ганц `index.html`. Гадны сан ашиглаагүй (Tailwind ч, GSAP ч байхгүй) —
зөвхөн фонт татагдана. Скролл дээр гарч ирэх эффектийг IntersectionObserver
хийдэг тул хуудас маш хөнгөн.

## Шинэ ажил нэмэх

`index.html`-ийн дээд талын `CONFIG.works` жагсаалтад нэг мөр нэмнэ.
Ажлын тоо, дараалал бүгд автоматаар шинэчлэгдэнэ.

```js
{
  title: 'Ажлын нэр',
  kind:  'Цахим урилга', year:'2026', tone:'lime',
  desc:  'Товч тайлбар.',
  tech:  ['GSAP'],
  live:  'https://ghostshdee.github.io/repo-нэр/',
  img:   'assets/repo-нэр.jpg',   // сонголт — доор «Зураг тавих» хэсгийг үз
  note:  ''
}
```

`tone` сонголт: `lime` `teal` `amber` `rose` `violet` `blue`

## Зураг тавих

Карт бүр анхдагчаар `tone` өнгөт хийсвэр дэвсгэртэй. Бодит зураг тавихдаа:

1. Зургаа `assets/` хавтсанд хийнэ (ж: `assets/dokay-portfolio.jpg`).
   Хэмжээ: **16:10 харьцаа**, 1200×750px орчим, JPG/WebP, 200–400 KB.
   Хамгийн амар арга — амьд сайт бүрийн дэлгэцийн зураг (screenshot) авах.
2. Тухайн ажлын `CONFIG.works` мөрөнд `img: 'assets/файл-нэр.jpg'` нэмнэ.
3. `img` байвал зураг, байхгүй бол `tone` өнгө гарна.

`<head>` доторх SEO болон Open Graph мета тагийг гараар шинэчилнэ —
Facebook, Messenger зэрэг crawler JavaScript ажиллуулдаггүй.
