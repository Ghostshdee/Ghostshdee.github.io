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
  code:  'https://github.com/Ghostshdee/repo-нэр',
  note:  ''
}
```

`tone` сонголт: `lime` `teal` `amber` `rose` `violet` `blue`

`<head>` доторх SEO болон Open Graph мета тагийг гараар шинэчилнэ —
Facebook, Messenger зэрэг crawler JavaScript ажиллуулдаггүй.
