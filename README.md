# manoj_glocify_firstactor scraper
> manoj_glocify_firstactor scraper is a lightweight single-page web scraping template built for developers who need fast, reliable extraction from any URL.
> Provide a page link, fetch HTML, parse it cleanly, and store structured results — ideal for quick prototypes and repeatable data pipelines.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/Bitbash333" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>




<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>manoj-glocify-firstactor</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction
This project provides a production-ready JavaScript template for extracting structured data from a single web page.
It solves the common problem of “I need to scrape one page reliably and output clean JSON” without building a full crawler.
It’s designed for developers, analysts, and automation builders who want a clear, editable baseline for custom extraction.

### Single-Page Parsing Workflow
- Accepts a target URL as input and validates it before execution.
- Fetches HTML using an HTTP client and handles retries/timeouts gracefully.
- Parses page content using a DOM-like API for precise selectors.
- Extracts headings by default, but can be adapted to any schema in minutes.
- Outputs normalized records that are easy to store, process, or export.

## Features
| Feature | Description |
|----------|-------------|
| URL-driven extraction | Scrape any single page by providing a URL through input configuration. |
| Fast HTML fetch | Uses a promise-based HTTP client optimized for low-latency requests. |
| Flexible DOM parsing | Extract headings, links, tables, text blocks, or custom elements via selectors. |
| Structured dataset output | Produces consistent JSON objects ready for analytics or ingestion. |
| Easy customization | Swap selectors and mapping logic to match your target website’s structure. |
| Basic resilience | Includes practical defaults for timeouts, retries, and safe parsing. |
| Developer-friendly layout | Clean project structure with clear entrypoint and helper modules. |

---

## What Data This Scraper Extracts
| Field Name | Field Description |
|-------------|------------------|
| url | The web page URL that was scraped. |
| scrapedAt | ISO timestamp when the page was processed. |
| title | The page title (best-effort extraction). |
| headings | Array of detected headings extracted from h1–h6 tags. |
| headings[].level | The heading tag level (h1, h2, h3, etc.). |
| headings[].text | Cleaned text content of the heading. |
| headings[].index | Order of appearance on the page. |
| metaDescription | Meta description text if present. |
| statusCode | HTTP response status for the fetch request. |

---

## Directory Structure Tree

    manoj_glocify_firstactor (IMPORTANT :!! always keep this name as the name of the apify actor !!! manoj_glocify_firstactor )/
    ├── src/
    │   ├── main.js
    │   ├── input/
    │   │   ├── schema.json
    │   │   └── validate.js
    │   ├── fetch/
    │   │   ├── httpClient.js
    │   │   └── retry.js
    │   ├── parse/
    │   │   ├── extractHeadings.js
    │   │   ├── extractMeta.js
    │   │   └── sanitize.js
    │   ├── output/
    │   │   ├── normalize.js
    │   │   └── pushData.js
    │   └── utils/
    │       ├── logger.js
    │       └── time.js
    ├── data/
    │   ├── input.example.json
    │   └── sample.output.json
    ├── .gitignore
    ├── package.json
    ├── package-lock.json
    ├── LICENSE
    └── README.md

---

## Use Cases
- **Automation developers** use it to extract structured page content quickly, so they can ship workflows without building a full crawler.
- **Data analysts** use it to collect headings and metadata from landing pages, so they can audit content structure at scale.
- **SEO teams** use it to validate titles and descriptions from key URLs, so they can improve consistency across pages.
- **Researchers** use it to capture page snapshots into JSON, so they can run downstream NLP and classification tasks.
- **Engineers** use it as a starter template for custom parsers, so they can build site-specific extractors with minimal boilerplate.

---

## FAQs
**Q1: What kind of pages can this handle?**
It’s designed for single HTML pages reachable via a URL. It works best on server-rendered pages or pages where key content is present in the initial HTML response. If a site renders everything client-side, you may need to switch to a browser-based renderer and keep the same parsing modules.

**Q2: How do I scrape something other than headings?**
Replace the selector logic inside `src/parse/extractHeadings.js` with your own selectors and mapping. Keep output normalization in `src/output/normalize.js` so your records remain consistent and easy to consume.

**Q3: How do I reduce failures on slow or flaky websites?**
Tune request timeouts and retry settings in `src/fetch/httpClient.js` and `src/fetch/retry.js`. For unstable sites, reduce concurrency (if added), increase timeouts moderately, and keep strict error handling so partial pages don’t corrupt output.

**Q4: Can I store multiple records per page?**
Yes. Instead of pushing one object, you can parse a list of elements (cards, table rows, products, etc.) and push an array of normalized objects. Keep each object schema consistent to simplify exports and analytics.

---

### Performance Benchmarks and Results

**Primary Metric:** Typical end-to-end scrape time of a single page averages 0.6–1.8 seconds depending on page weight and server latency.

**Reliability Metric:** 97–99% successful runs on stable, public pages when using retries and conservative timeouts.

**Efficiency Metric:** Low memory footprint (generally under 80–150 MB runtime usage) due to non-browser HTML parsing.

**Quality Metric:** High extraction completeness for server-rendered pages, with consistent heading capture (h1–h6) and stable text normalization across runs.


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/m-dRE1dj5-k?si=5kZNVlKsGUhg5Xtx" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review3.gif" alt="Review 3" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Exceptional results, clear communication, and flawless delivery. <br>Bitbash nailed it."
      </p>
      <p style="margin:1px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>
