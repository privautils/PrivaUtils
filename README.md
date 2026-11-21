# PrivaUtils

> Free, private, client-side developer utilities and document processing tools executing 100% in local browser memory. Zero cloud uploads, zero wait queues, zero telemetry.

**Website**: [https://privautils.com](https://privautils.com)  
**Stack**: Next.js 16, React 19, TypeScript 5, Tailwind CSS, Web Workers, WebAssembly, Cloudflare Workers  

---

PrivaUtils is an open suite of 18 single-purpose utilities engineered for developers, security professionals, and content creators. Every operation (JSON parsing, PDF page manipulation, cryptographic hashing, and regular expression evaluation) runs entirely on your local machine using dedicated Web Workers, WebAssembly, and native WebCrypto APIs. No files, text payloads, JWT tokens, or strings are ever transmitted to an external server.

---

## Online Tools Directory

Access the live tools directly at [privautils.com](https://privautils.com):

### Developer & Coding Tools

* [JSON Formatter & Tree Viewer](https://privautils.com/coding/json-formatter): Format, validate, and inspect JSON payloads with lossless 64-bit BigInt precision, dynamic indentation, and branch collapsing.
* [Base64 Converter](https://privautils.com/coding/base64-converter): Encode and decode text strings, binary files, and data URIs locally.
* [JWT Token Inspector](https://privautils.com/coding/jwt-inspector): Decode JOSE headers and payload claims with in-browser WebCrypto signature verification.
* [URL & HTML Entity Encoder](https://privautils.com/coding/url-encoder): RFC 3986 URI encoding and WHATWG HTML entity conversion.
* [RegEx Tester & Debugger](https://privautils.com/coding/regex-tester): Test ECMAScript regular expressions inside a sandboxed Web Worker with a 200ms ReDoS timeout guard.
* [Crontab Builder & Generator](https://privautils.com/coding/crontab-builder): Visual cron schedule editor with human-readable syntax breakdown and upcoming execution schedules.

### PDF & Document Tools

* [PDF Splitter](https://privautils.com/document/pdf-splitter): Split PDF pages or extract custom page ranges into standalone files and ZIP archives in local RAM.
* [PDF Merger](https://privautils.com/document/pdf-merger): Combine multiple PDF documents and image files into a single document without cloud uploads.
* [PDF Rotator](https://privautils.com/document/pdf-rotator): Rotate PDF pages by 90, 180, or 270 degrees with lossless output.
* [Image to PDF Converter](https://privautils.com/document/image-to-pdf): Convert PNG, JPG, and WebP images into formatted PDF documents in browser memory.

### Text & Content Tools

* [SEO Slug Generator](https://privautils.com/text/slug-generator): Generate URL-safe slugs with Unicode transliteration and custom delimiter controls.
* [Bionic Reading Converter](https://privautils.com/text/bionic-reading): Convert text into bionic reading format to improve reading speed and comprehension.
* [Case Converter](https://privautils.com/text/case-converter): Convert text between camelCase, PascalCase, snake_case, kebab-case, Title Case, and uppercase.
* [Text Metrics & Word Counter](https://privautils.com/text/text-metrics): Measure word count, character count, estimated reading time, and readability scores.
* [Whitespace Sanitizer](https://privautils.com/text/whitespace-sanitizer): Strip duplicate spacing, clean trailing line breaks, and remove hidden zero-width unicode artifacts.

### Security & Cryptography Tools

* [Hash Generator & HMAC Signer](https://privautils.com/security/hash-generator): Compute MD5, SHA-1, SHA-256, SHA-512 hashes and HMAC signatures using hardware-accelerated WebCrypto.
* [Secure Password Generator](https://privautils.com/security/password-generator): Generate high-entropy passwords and passphrases using browser cryptographic random number generation (CSPRNG).
* [UUID Generator](https://privautils.com/security/uuid-generator): Generate batch RFC 4122 v4 UUIDs, time-ordered UUID v7s, and ULIDs.

### Tool Comparisons & Privacy Alternatives

* [10015.io Alternative](https://privautils.com/compare/10015-alternative): Complete zero-tracking developer toolbox alternative with local IndexedDB vault.
* [CyberChef Alternative](https://privautils.com/compare/cyberchef-alternative): Modern, mobile-responsive developer utility suite with WebCrypto hardware acceleration.
* [Smallpdf Alternative](https://privautils.com/compare/smallpdf-alternative): Free client-side PDF manipulation with no daily quotas, paywalls, or cloud uploads.
* [iLovePDF Alternative](https://privautils.com/compare/ilovepdf-alternative): Private zero-upload PDF suite with visual storyboard page assembly and total data privacy.

---

## Core Architecture

* **Zero Backend Compute**: All file transformations and computations occur in the user's browser thread or Web Workers. The server serves only static assets.
* **Lossless 64-bit Integer Precision**: The JSON parser preserves Snowflake IDs (Discord, Twitter, Mastodon) and arbitrary 64-bit integers without IEEE 754 floating-point truncation.
* **Sandboxed Worker Isolation**: CPU-heavy tasks run in background Web Workers via Comlink RPC, keeping the main UI thread at 60 FPS.
* **Memory Management**: Large binary buffers use transferable ArrayBuffers to avoid memory leaks and browser crashes during PDF operations.
* **Layout Stability**: Pre-allocated CSS aspect ratios guarantee Cumulative Layout Shift (CLS) remains at 0.00.

---

## Machine-Readable Specifications for AI & LLMs

* Full documentation for AI search bots: [https://privautils.com/llms.txt](https://privautils.com/llms.txt)
* Complete technical catalog: [https://privautils.com/llms-full.txt](https://privautils.com/llms-full.txt)
