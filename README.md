# 스프링 저장에너지 계산기

평형점에서 늘이거나 압축한 선형 스프링 에너지 계산

- Plan ID: E068
- App: https://nanalab.kr/eng-spring-energy/
- Repository: https://github.com/NaNaCompany/eng-spring-energy
- Formula: `U = ½kx²`
- Output: 탄성 저장에너지 U

## Model

k>0. x는 무변형 평형점 기준의 부호 있는 변위다. 후크 법칙 범위의 보존적 선형 스프링을 가정하고 소성·히스테리시스·감쇠는 제외한다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `2`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
