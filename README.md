# Doavers - Next JS (App Router, Typescript)

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

---

## Requirement

- Node JS v16
- Fake API Posts (<https://jsonplaceholder.typicode.com/posts>)
- Fake API Products (<https://fakestoreapi.com/products>)

---

## Installation and Basic Setup

```sh
npx create-next-app@latest nextjs-approuter
cd nextjs-approuter

√ Would you like to use TypeScript with this project? ... Yes
√ Would you like to use ESLint with this project? ... Yes
√ Would you like to use Tailwind CSS with this project? ... Yes
√ Would you like to use `src/` directory with this project? ... No
√ Use App Router (recommended)? ... Yes
√ Would you like to customize the default import alias? ... Yes
√ What import alias would you like to configured? ... @/*

# Path alias akan tersimpan di file ./jsconfig.json

# Install dependency
npm install axios next-auth moment prisma @prisma/client swr uuid @types/uuid zod openai bcryptjs @types/bcryptjs
npm install react-hot-toast react-icons next-themes

```

---

## Penjelasan Dependency

```sh
# Installing sass
npm install sass

# Buat folder dan file di ./styles/sass/main.scss
# Buat folder dan file di ./styles/sass/base/index.scss
# Update postcss.config.js

# Install postcss plugins
npm install postcss-import cssnano postcss-plugin

# Data fetching https://jsonplaceholder.typicode.com/posts
npm install axios

# Edit pages/_app.js
# Jalankan script
npm run dev

# Untuk SSR
npm run build

# Untuk run production bisa pakai
npm run start

# Untuk membantu melakukan validasi tipe data bisa menginstall prop-types
npm install prop-types

# Untuk membuat Next API, melakukan validasi API
npm install next-connect@0.13.0
npm install joi@17.7.1  next-joi@2.2.1

# Untuk membantu membuat halaman login bisa menggunakan next-auth
npm install next-auth
# Install moment untuk kebutuhan handling date time
npm install moment

# Untuk Database ORM bisa menggunakan Prisma
npm install prisma @prisma/client
# Buat file .env terlebih dahulu, silakan cek examplenya
npx prisma
npx prisma init
# Edit file di ./prisma/schema.prisma
npx prisma format
npx prisma validate
npx prisma migrate dev --preview-feature
# Bisa juga langsung tanpa migrate dev (Code First) without migrate
npx prisma db push
# Jika sudah ada DB (DB First)
npx prisma db pull

# Jika mau menggunakan SWR
npm install swr

# Install VS Code extension "REST CLient" kemudian buat file .\test-api.rest
# Lakukan test api menggunakan file *.rest

# git push notes
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_rsa
```

---

## Dockerize Next JS App

```sh
# Create Dockerfile
export GHCR_PAT=YOUR_GITHUB_PERSONAL_ACCESS_TOKEN
echo $GHCR_PAT | docker login ghcr.io --username doavers --password-stdin
cat ~/.docker/config.json
docker build -t ghcr.io/username/package-name:latest .
docker push ghcr.io/username/package-name:latest
docker run -p host_port:container_port ghcr.io/username/package-name:latest
```

---

## Reference

- [Next JS Docs](https://nextjs.org/docs)
- [Next Auth Docs](https://next-auth.js.org/getting-started/introduction)
- [Prisma ORM Docs](https://www.prisma.io/docs)
- [Supabase Free Postgres Online DB](https://supabase.com/)
- [Create Docker Image for Next JS-](https://blog.tericcabrel.com/create-docker-image-nextjs-application/)
- [Next JS Template on Vercel](https://vercel.com/templates?framework=next.js)
- [IP Blocking with Upstash](https://vercel.com/templates/next.js/ip-blocking)
- [Edge Function Geolocation](https://vercel.com/templates/next.js/edge-functions-geolocation)
- [Edge Function i18n](https://vercel.com/templates/next.js/edge-functions-i18n)
- [Vercel Blob Image Starter](https://vercel.com/templates/next.js/blob-starter)
