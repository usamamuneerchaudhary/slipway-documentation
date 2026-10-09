# Slipway documentation

Source for the [Slipway docs site](https://laravel-slipway.mintlify.site/).

Slipway is a Laravel package that treats `config/slipway.php` as the single source of truth for CI/CD. The provider YAML files are generated from it, committed, and guarded.

Package repository: [usamamuneerchaudhary/laravel-slipway](https://github.com/usamamuneerchaudhary/laravel-slipway).

## Preview locally

```bash
npx mint dev
```

Open [http://localhost:3000](http://localhost:3000). Run this from the directory that contains `docs.json`.

If the preview is stale, run `npx mint update`.

## Publishing

Changes on the default branch deploy to [https://laravel-slipway.mintlify.site/](https://laravel-slipway.mintlify.site/).
