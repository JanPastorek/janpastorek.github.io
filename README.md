# janpastorek.com

Personal academic website of Jan Pastorek, built with [Quartz](https://quartz.jzhao.xyz/).

Content lives in `content/`. To preview locally:

```bash
npm i
npx quartz build --serve
```

To publish, push to `master` — a GitHub Actions workflow (`.github/workflows/deploy.yml`) builds the site and deploys it to GitHub Pages automatically.
