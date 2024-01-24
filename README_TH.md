# 🚀 AstroWind

<img src="https://raw.githubusercontent.com/onwidget/.github/main/resources/astrowind/lighthouse-score.png" align="right"
     alt="AstroWind Lighthouse Score" width="100" height="358">

🌟 ธีม Astro ที่ติดดาวและแยกมากที่สุดในปี 2022 และ 2023 🌟

#### **AstroWind** คือ เทมเพลตโอเพ่นซอร์ส ฟรี สำหรับสร้างเว็บไซต์ของคุณโดยใช้ [Astro 4.0](https://astro.build/)+[Tailwind CSS](https://tailwindcss.com/). พร้อมสำหรับการเริ่มโครงการใหม่และออกแบบ โดยคำนึงถึงแนวทางปฏิบัติที่ดีที่สุดสำหรับเว็บ.


##### <div align="center">ภาษาไทย || [English](./README.md) 
##### <div align="center">คู่มือนี้ปรับเเต่งบางอย่างเพื่อให้ผู้ใช้ในท้องถิ่น เข้าถึงโดยง่าย Cr [ปรีดิ์ปราโมทย์](./Mint&Mu.md)


- ✅ คะแนน พร้อมการผลิตในรายงานPageSpeed ​​Insights
- ✅ บูรณาการกับTailwind CSSรองรับโหมด DarkและRTL
- ✅ บล็อกที่รวดเร็วและเป็นมิตรกับ SEOพร้อมฟีด RSS อัตโนมัติ , รองรับMDX , หมวดหมู่และแท็ก , การแบ่งปันทางสังคม , ...
- ✅ การเพิ่มประสิทธิภาพรูปภาพ (ใช้สินทรัพย์ Astro ใหม่ และUnpicสำหรับ Universal image CDN)
- ✅ การสร้างแผนผังเว็บไซต์โครงการตามเส้นทางของคุณ
- ✅ เปิดแท็กกราฟสำหรับการแชร์บนโซเชียลมีเดีย
- ✅ Analyticsในตัว Google Analytics และการรวม Splitbee

  <br>

<img src="https://raw.githubusercontent.com/onwidget/.github/main/resources/astrowind/screenshot-astro4.png" alt="AstroWind Theme Screenshot">

[![onWidget](https://custom-icon-badges.demolab.com/badge/made%20by%20-onWidget-556bf2?style=flat-square&logo=onwidget&logoColor=white&labelColor=101827)](https://onwidget.com)
[![License](https://img.shields.io/github/license/onwidget/astrowind?style=flat-square&color=dddddd&labelColor=000000)](https://github.com/onwidget/astrowind/blob/main/LICENSE.md)
[![Maintained](https://img.shields.io/badge/maintained%3F-yes-brightgreen.svg?style=flat-square)](https://github.com/onwidget)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat-square)](https://github.com/onwidget/astrowind#contributing)
[![Known Vulnerabilities](https://snyk.io/test/github/onwidget/astrowind/badge.svg?style=flat-square)](https://snyk.io/test/github/onwidget/astrowind)
[![Stars](https://img.shields.io/github/stars/onwidget/astrowind.svg?style=social&label=stars&maxAge=86400&color=ff69b4)](https://github.com/onwidget/astrowind)
[![Forks](https://img.shields.io/github/forks/onwidget/astrowind.svg?style=social&label=forks&maxAge=86400&color=ff69b4)](https://github.com/onwidget/astrowind)

<br>

<details open>
<summary>Table of Contents</summary>

- [Demo](#demo)
- [Getting started](#getting-started)
  - [Project structure](#project-structure)
  - [Commands](#commands)
  - [Configuration](#configuration)
  - [Deploy](#deploy)
- [Frequently Asked Questions](#frequently-asked-questions)
- [Related Projects](#related-projects)
- [Contributing](#contributing)
- [Acknowledgements](#acknowledgements)
- [License](#license)

</details>

<br>

## Demo

📌 [https://astrowind.vercel.app/](https://astrowind.vercel.app/)

<br>

## เริ่มต้นใช้งาน
AstroWindพยายามให้คุณเข้าถึงการสร้างเว็บไซต์ได้อย่างรวดเร็วโดยใช้Astro 4.0 + Tailwind CSS เป็นธีมฟรีที่เน้นความเรียบง่าย แนวทางปฏิบัติที่ดี และประสิทธิภาพสูง

จาวาสคริปต์วานิลลาน้อยมากถูกใช้เพื่อให้ฟังก์ชันพื้นฐานเท่านั้น เพื่อให้นักพัฒนาแต่ละคนตัดสินใจว่าจะใช้เฟรมเวิร์กใด (React, Vue, Svelte, Solid JS...) และวิธีบรรลุเป้าหมาย

โครงสร้างโครงการ
ภายใน เทมเพลต AstroWindคุณจะเห็นโฟลเดอร์และไฟล์ต่อไปนี้:

```
/
├── public/
│   ├── _headers
│   └── robots.txt
├── src/
│   ├── assets/
│   │   ├── favicons/
│   │   ├── images/
│   │   └── styles/
│   │       └── tailwind.css
│   ├── components/
│   │   ├── blog/
│   │   ├── common/
│   │   ├── ui/
│   │   ├── widgets/
│   │   │   ├── Header.astro
│   │   │   └── ...
│   │   ├── CustomStyles.astro
│   │   ├── Favicons.astro
│   │   └── Logo.astro
│   ├── content/
│   │   ├── post/
│   │   │   ├── post-slug-1.md
│   │   │   ├── post-slug-2.mdx
│   │   │   └── ...
│   │   └-- config.ts
│   ├── layouts/
│   │   ├── Layout.astro
│   │   ├── MarkdownLayout.astro
│   │   └── PageLayout.astro
│   ├── pages/
│   │   ├── [...blog]/
│   │   │   ├── [category]/
│   │   │   ├── [tag]/
│   │   │   ├── [...page].astro
│   │   │   └── index.astro
│   │   ├── index.astro
│   │   ├── 404.astro
│   │   ├-- rss.xml.ts
│   │   └── ...
│   ├── utils/
│   ├── config.yaml
│   └── navigation.js
├── package.json
├── astro.config.mjs
└── ...
```

Astro ค้นหา`.astro` or `.md` files in the `src/pages/` directory. แต่ละหน้าจะแสดงเป็นเส้นทางตามชื่อไฟล์

ไม่มีอะไรพิเศษเกี่ยวกับ `src/components/`, แต่นั่นคือสิ่งที่เราต้องการใส่ส่วนประกอบ Astro/React/Vue/Svelte/Preact

สินทรัพย์คงที่ใดๆ เช่น รูปภาพ สามารถวางลงใน `public/` directory ได้หากไม่ต้องการการแปลงใดๆ หรือใน `assets/` directory หากนำเข้าโดยตรง  

[![Edit AstroWind on CodeSandbox](https://codesandbox.io/static/img/play-codesandbox.svg)](https://githubbox.com/onwidget/astrowind/tree/main) [![Open in Gitpod](https://svgshare.com/i/xdi.svg)](https://gitpod.io/?on=gitpod#https://github.com/onwidget/astrowind) [![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/onwidget/astrowind)

> 🧑‍🚀 **Seasoned astronaut?** Delete this file `README.md`. Update `src/config.yaml` and contents. Have fun!

<br>

### Commands

คำสั่งทั้งหมดถูกรันจาก root of the project, จาก terminal:

| Command               | Action                                             |
| :-------------------- | :------------------------------------------------- |
| `npm install`         | ติดตั้งการพึ่งพา                             |
| `npm run dev`         | เริ่มเซิร์ฟเวอร์ dev ในเครื่องที่ `localhost:3000`        |
| `npm run build`       | ไซต์การผลิตของคุณ มองหาที่ `./dist/`            |
| `npm run preview`     | ดูตัวอย่างงานสร้างของคุณภายในเครื่องก่อนที่จะปรับใช้       |
| `npm run format`      | จัดรูปแบบโค้ดด้วย Prettier                         |
| `npm run lint:eslint` | Run Eslint                                         |
| `npm run astro ...`   | Run CLI commands like `astro add`, `astro preview` |

<br>

### Configuration

พื้นฐาน configuration file: `./src/config.yaml`

```yaml
site:
  name: 'Example'
  site: 'https://example.com'
  base: '/' # Change this if you need to deploy to Github Pages, for example
  trailingSlash: false # Generate permalinks with or without "/" at the end

  googleSiteVerificationId: false # Or some value,

# Default SEO metadata
metadata:
  title:
    default: 'Example'
    template: '%s — Example'
  description: 'This is the default meta description of Example website'
  robots:
    index: true
    follow: true
  openGraph:
    site_name: 'Example'
    images:
      - url: '~/assets/images/default.jpg'
        width: 1200
        height: 628
    type: website
  twitter:
    handle: '@twitter_user'
    site: '@twitter_user'
    cardType: summary_large_image

i18n:
  language: en
  textDirection: ltr

apps:
  blog:
    isEnabled: true # If the blog will be enabled
    postsPerPage: 6 # Number of posts per page

    post:
      isEnabled: true
      permalink: '/blog/%slug%' # Variables: %slug%, %year%, %month%, %day%, %hour%, %minute%, %second%, %category%
      robots:
        index: true

    list:
      isEnabled: true
      pathname: 'blog' # Blog main path, you can change this to "articles" (/articles)
      robots:
        index: true

    category:
      isEnabled: true
      pathname: 'category' # Category main path /category/some-category, you can change this to "group" (/group/some-category)
      robots:
        index: true

    tag:
      isEnabled: true
      pathname: 'tag' # Tag main path /tag/some-tag, you can change this to "topics" (/topics/some-category)
      robots:
        index: false

    isRelatedPostsEnabled: true # If a widget with related posts is to be displayed below each post
    relatedPostsCount: 4 # Number of related posts to display

analytics:
  vendors:
    googleAnalytics:
      id: null # or "G-XXXXXXXXXX"

ui:
  theme: 'system' # Values: "system" | "light" | "dark" | "light:only" | "dark:only"
```

<br>

### Deploy

#### Deploy to production (manual)

คุณสามารถสร้างบิลด์การผลิตที่ได้รับการปรับปรุงด้วย:


```shell
npm run build
```

ตอนนี้เว็บไซต์ของคุณพร้อมที่จะใช้งานแล้ว ไฟล์ที่สร้างขึ้นทั้งหมดจะอยู่ที่
`dist` folder,ซึ่งคุณสามารถปรับใช้โฟลเดอร์กับบริการโฮสติ้งใดๆ ที่คุณต้องการได้
prefer.

#### Deploy to Netlify

โคลนพื้นที่เก็บข้อมูลนี้ในบัญชี GitHub ของตัวเองและปรับใช้กับ Netlify:

[![Netlify Deploy button](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/onwidget/astrowind)

#### Deploy to Vercel

โคลนพื้นที่เก็บข้อมูลนี้ในบัญชี GitHub ของตัวเองและปรับใช้กับ Vercel:


[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fonwidget%2Fastrowind)

<br>

## Frequently Asked Questions

- Why?
-
-

<br>

## Related projects

- [TailNext](https://tailnext.vercel.app/) - Free template using Next.js 14 and Tailwind CSS with the new App Router.
- [Qwind](https://qwind.pages.dev/) - Free template to make your website using Qwik + Tailwind CSS.

## Contributing

หากคุณมีความคิด ข้อเสนอแนะ หรือพบข้อบกพร่องใดๆ อย่าลังเลที่จะเปิดการสนทนา ปัญหา หรือสร้างคำขอดึงข้อมูล นั่นจะเป็นประโยชน์มากสำหรับเราทุกคน และเรายินดีที่จะรับฟังและดำเนินการ

## Acknowledgements

Initially created by [onWidget](https://onwidget.com) and maintained by a community of [contributors](https://github.com/onwidget/astrowind/graphs/contributors).

## License

**AstroWind** ด้รับใบอนุญาตภายใต้ใบอนุญาต MIT — ดู ไฟล์ [LICENSE](./LICENSE.md) ใบอนุญาต สำหรับรายละเอียด






  
