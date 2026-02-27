# SyntraFlow AI

Platforma web moderna construita pentru proiectul de licenta:

**"Dezvoltarea unei platforme web moderne cu asistent virtual pentru automatizarea proceselor"**

Aplicatia prezinta un website enterprise-style, complet original, cu accent pe:

- asistent virtual demonstrativ
- automatizarea proceselor de contact si suport
- lead capture si cereri de oferta
- FAQ inteligent
- prezentare tehnica si academica a arhitecturii

## Contextul proiectului

SyntraFlow AI este gandit ca un demo de licenta care arata ca un produs real, nu doar ca o pagina de prezentare. Structura este pregatita pentru:

- sustinere academica
- portofoliu full-stack / UI-UX
- demo de produs
- extindere ulterioara intr-o platforma SaaS

## Stack tehnologic

- Next.js 16.1.6
- React 19.2.4
- TypeScript 5.9.3
- Tailwind CSS 4.2.1
- App Router

## Functionalitati incluse

- homepage premium cu sectiuni enterprise
- navigatie sticky cu meniu mobil
- pagini dedicate pentru solutii, industrii, asistent virtual, automatizari, arhitectura si studii de caz
- demo conversational front-end only
- FAQ accordion
- contact form cu validare, loading, succes si eroare simulata
- stat counters animate
- metadata SEO, `robots.ts` si `sitemap.ts`
- componente reutilizabile si continut data-driven

## Structura folderelor

```text
.
|-- app
|   |-- about... (rute App Router)
|   |-- globals.css
|   |-- icon.svg
|   |-- layout.tsx
|   |-- not-found.tsx
|   |-- page.tsx
|   |-- robots.ts
|   `-- sitemap.ts
|-- components
|   |-- layout
|   |-- sections
|   `-- ui
|-- lib
|   |-- site-config.ts
|   |-- site-data.ts
|   `-- utils.ts
|-- public
|   `-- og-image.svg
|-- .env.example
|-- next.config.ts
|-- package.json
|-- postcss.config.mjs
`-- tsconfig.json
```

## Instalare

1. Instaleaza dependintele:

```bash
npm install
```

2. Copiaza valorile de mediu:

```bash
copy .env.example .env.local
```

3. Ruleaza proiectul in development:

```bash
npm run dev
```

Aplicatia va fi disponibila implicit la `http://localhost:3000`.

## Scripturi utile

- `npm run dev` - porneste serverul local
- `npm run build` - genereaza build-ul de productie
- `npm run start` - porneste build-ul generat
- `npm run check` - ruleaza verificarea TypeScript fara emitere

## Personalizare

- Continutul principal este definit in `lib/site-data.ts`.
- Configuratia de branding si metadata este in `lib/site-config.ts`.
- Stilurile globale si directia vizuala sunt in `app/globals.css`.
- Homepage-ul este compus in `components/sections/home-page.tsx`.

## Note privind formularul si demo-ul

- Formularul de contact foloseste validare client-side.
- Trimiterea este simulata printr-un delay artificial.
- Daca emailul contine textul `eroare`, formularul afiseaza starea de eroare pentru demonstratie.
- Demo-ul de chat este front-end only si ruleaza pe seturi de mesaje presetate.

## Posibile extensii viitoare

- integrare cu backend real pentru stocarea lead-urilor
- conectare la CRM sau email transactional
- integrare cu un model AI real si knowledge base actualizabila
- autentificare pentru zona administrativa
- analytics si dashboard de conversii

## Deploy

Aplicatia poate fi publicata pe:

- Vercel
- Netlify (cu configurare compatibila Next.js)
- orice infrastructura capabila sa ruleze `next build` si `next start`

Pentru productie, seteaza `NEXT_PUBLIC_SITE_URL` la domeniul final in `.env.local`.
