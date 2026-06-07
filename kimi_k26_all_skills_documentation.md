# Dokumentasi Lengkap: Semua Skill dalam Sistem Kimi K2.6 Agent Swarm

> **Versi:** 2026-05-13  
> **Total Skill Terdokumentasi:** 260+ skill  
> **Sumber:** `/app/.agents/skills/` (built-in) + `/app/.user/skills/` (user-defined)  

---

## Daftar Isi

1. [Ringkasan Kategori Skill](#1-ringkasan-kategori-skill)
2. [Capability Skills (Inti)](#2-capability-skills-inti)
3. [Artifact Skills (Output Format)](#3-artifact-skills-output-format)
4. [Research & Analysis Skills](#4-research--analysis-skills)
5. [Writing & Content Creation Skills](#5-writing--content-creation-skills)
6. [Coding & Development Skills](#6-coding--development-skills)
7. [Financial & Trading Skills](#7-financial--trading-skills)
8. [Business & Marketing Skills](#8-business--marketing-skills)
9. [Design & Visualization Skills](#9-design--visualization-skills)
10. [Data & Analytics Skills](#10-data--analytics-skills)
11. [Communication & Productivity Skills](#11-communication--productivity-skills)
12. [Security & Compliance Skills](#12-security--compliance-skills)
13. [Specialized Domain Skills](#13-specialized-domain-skills)
14. [Utility & Tool Skills](#14-utility--tool-skills)
15. [User-Defined Skills](#15-user-defined-skills)
16. [Struktur Direktori & Priority Rules](#16-struktur-direktori--priority-rules)

---

## 1. Ringkasan Kategori Skill

| Kategori | Jumlah | Fungsi Utama |
|----------|--------|-------------|
| Capability Skills (Inti) | 12 | Orchestrasi tugas kompleks (research, writing, coding, etc.) |
| Artifact Skills | 6 | Generasi output format (DOCX, PDF, XLSX, PPTX, dll.) |
| Research & Analysis | 45 | Riset mendalam, analisis data, statistik, SEO |
| Writing & Content | 38 | Penulisan kreatif, akademik, marketing, copywriting |
| Coding & Development | 32 | Coding, review, testing, arsitektur, DevOps |
| Financial & Trading | 28 | Analisis saham, ETF, DCF, valuasi, laporan keuangan |
| Business & Marketing | 26 | Strategi bisnis, pricing, campaign, email, resume |
| Design & Visualization | 18 | Infografik, timeline, chart, magazine, UI blueprint |
| Data & Analytics | 16 | Database, SQL, dataset audit, regresi, outlier detection |
| Communication & Productivity | 22 | Email, meeting, speech, OKR, work report, interview |
| Security & Compliance | 12 | OWASP audit, legal risk, ISO 27001, ToS scanner |
| Specialized Domain | 15 | Astronomi, mode, podcast, video, gravitasi, dll. |
| Utility & Tool | 12 | Browser, scraper, TTS, git, kubectl, terraform |
| User-Defined Skills | 4 | Trading education, coding discipline |

**Total: 260+ skill terdokumentasi**

---

## 2. Capability Skills (Inti)

Skill ini adalah **skill orkestrasi utama** yang mengendalikan alur kerja multi-agent.


### deep-research-swarm
- **Deskripsi:** Orchestrasi riset mendalam multi-agent dengan adaptive routing (4 route: A/B/C/D)
- **Trigger:** Research, investigation, in-depth analysis, trend analysis, competitive analysis
- **Route A:** Wide Search — topik luas/eksploratif
- **Route B:** Focused Search — pertanyaan spesifik dengan dimensi jelas
- **Route C:** File-Only Research — analisis hanya dari file yang diunggah
- **Route D:** File-Augmented Research — analisis file utama + sumber eksternal

### deep-research
- **Deskripsi:** Riset mendalam evidence-based dengan minimum 10-iteration search cycle
- **Trigger:** Comprehensive research, evidence-backed reports, quantitative visualization
- **Output:** Laporan terstruktur >10,000 kata dengan visualisasi IPython

### report-writing
- **Deskripsi:** End-to-end pembuatan laporan panjang (industry research, market analysis, policy briefs, white papers)
- **Trigger:** Write/draft/create report, analysis document, research brief
- **Output:** Markdown (`.md`) format

### paper-writing
- **Deskripsi:** End-to-end academic paper creation (survey papers, empirical research, literature reviews)
- **Trigger:** Write academic paper, conference submission, journal article, thesis chapter
- **Output:** Markdown (`.md`) format dengan metodologi formal

### general-writing
- **Deskripsi:** Entry point untuk semua creative writing genres (fiction, poetry, lyrics, drama, screenplay, essay, game writing)
- **Trigger:** Creative writing requests — novels, poems, scripts, essays
- **Output:** Manuscript (.docx + .md) melalui subagent orchestration

### vibecoding-general-swarm
- **Deskripsi:** Orchestrasi coding umum — **MANDATORY** untuk semua tugas coding non-web
- **Trigger:** Python tools, data pipelines, ML systems, APIs, games, bots, CLI apps
- **Mode:** Mode A (multi-agent, 3+ modul) dan Mode B (single agent)

### vibecoding-webapp-swarm
- **Deskripsi:** Multi-agent webapp building dengan design-first React workflow
- **Trigger:** Websites, landing pages, dashboards, browser games
- **Tech Stack:** Node.js 20, Tailwind v3, Vite v7, React 19 + TypeScript

### webapp-building-swarm
- **Deskripsi:** Multi-agent architecture untuk React webapps dengan git worktrees dan parallel development
- **Trigger:** Building webapps dalam konteks swarm dengan parallel branch development
- **Template:** 13 design templates tersedia

### webapp-building
- **Deskripsi:** Tools untuk building React web applications dengan TypeScript, Tailwind CSS, shadcn/ui
- **Trigger:** Single-page application atau interactive website menggunakan React + TypeScript

### batch-download
- **Deskripsi:** Multi-agent batch download dan data collection dengan parallel sub-agents
- **Trigger:** Discovering, validating, downloading multiple files/datasets dari web
- **Workflow:** 4-phase (Plan → Evidence Gathering → Parallel Download → Integration)

### skill-creator-swarm
- **Deskripsi:** Panduan pembuatan skill dalam environment agent swarm dengan evaluasi multi-agent
- **Trigger:** Create new skill, update existing skill, refine through swarm evaluation

### skill-creator
- **Deskripsi:** Panduan pembuatan skill efektif yang memperluas kemampuan agent
- **Trigger:** Create new skill atau update existing skill

---

## 3. Artifact Skills (Output Format)

Skill ini menangani **generasi output dalam format spesifik**.


### docx
- **Deskripsi:** Create dan edit Word documents menggunakan C# + OpenXML SDK (creation) dan WIR engine (editing)
- **Trigger:** Any .docx task — creation, editing, comments, revisions, TOC, Markdown-to-Word
- **Capabilities:** Three routing modes (WIR/md2docx/Create), OpenXML validation, native Word charts, OMML math equations

### pdf
- **Deskripsi:** Solusi PDF profesional — creation (HTML+Paged.js), processing (Python), LaTeX compilation
- **Trigger:** PDF creation, extraction, merging, LaTeX requests
- **Capabilities:** Math formulas, diagrams, tables, clickable cross-references

### xlsx
- **Deskripsi:** Manipulasi, analisis, dan pembuatan spreadsheet (XLSX, XLSM, CSV)
- **Trigger:** Excel creation, spreadsheet manipulation, financial modeling, pivot tables
- **Capabilities:** Formula deployment, complex formatting, data visualization, finance modeling

### pptx-swarm
- **Deskripsi:** Presentation skill dengan swarm/subagent support menggunakan PPTD DSL
- **Trigger:** Any PowerPoint/PPT/PPTX/slides requests
- **Restriction:** Main agent does design/outline/.pptd; subagents only generate .page files

### pptx
- **Deskripsi:** Presentation creation/editing menggunakan PPTD domain-specific language
- **Trigger:** Same as pptx-swarm — any presentation requests
- **Format:** .pptd files (YAML over OOXML)

### kimi-widget
- **Deskripsi:** Kimi widget design system dengan CSS variables, typography, layout rules, component patterns
- **Trigger:** Read BEFORE any show_widget call
- **Components:** Buttons 4 sizes, inputs, radio, checkbox, toggle, slider

---

## 4. Research & Analysis Skills


### academic-paper-reviewer
Simulasi peer review akademik mengevaluasi paper dari 4 dimensi (Originality, Methodology, Results, Writing) dengan skor 1-10 dan rekomendasi Major/Minor Revision.

### competitive-seo-intel
Analisis mendalam strategi SEO dan GEO competitor, mencakup keyword rankings, content tactics, backlink profiles, technical SEO, dan AI citation patterns.

### competitor-analysis
Analisis competitor SEO dan GEO — ranking keywords, content, backlinks, AI citations — untuk mengungkap peluang.

### deep-probe
连环追问 (serial probing) pada proposal/design, memeriksa setiap cabang decision tree satu per satu sampai konsensus tercapai.

### primary-market-research
PE/VC industry research reports (15-60 halaman) dengan analisis mendalam sektor TMT, consumer, healthcare, industrials.

### research-advisor
Scientific problem selection & decision trees berdasarkan framework Fischbach & Walsh (Cell, 2024).

### research-paper-refiner
Polishing academic paper English paragraph by paragraph, meninjau grammar, word choice, voice, coherence.

### research-writer
Penulisan research dengan section-by-section feedback, research assistance, citation management.

### scientific-problem-selection
Framework sistematis untuk pemilihan masalah penelitian ilmiah dengan 9 core skills dan decision tree navigation.

### vc-industry-research
PE/VC industry research reports dengan professional typography dan exhibit numbering.

### quick-event-etf-study
Event-driven concept ETF research + dashboard interaktif untuk A-shares dan US markets.

### quick-strategy-backtest
Trading strategy backtesting dengan dashboard HTML dan anti-look-ahead mechanisms.

### trading-strategy-backtest
Konversi deskripsi strategi ke runnable backtest code dengan lot-level accounting dan HTML dashboard.

### event-etf-study
ETF research berdasarkan key events — concept stock identification, market-cap-weighted indices, event window analysis.

### commodities-outlook
Laporan outlook komoditas institutional-grade (energy, metals, agriculture) dalam format PDF/DOCX/PPTX.

### commodity-research-outlook
Versi Chinese dari commodities-outlook dengan analisis supply-demand dan price forecasts.

### market-insight-report
Market insight reports bergaya top-tier consulting firm dengan executive summaries dan trend analysis.

### market-research-brief
Versi English dari market-insight-report dengan 6 analytical frameworks dan 9 chart types.

### equity-research
Analisis perusahaan dan riset investasi untuk China A-shares, HK, US stocks — Tear Sheet dan Equity Report modes.

### equity-researcher
Institutional-grade investment research dengan DCF valuation, comparable analysis, sensitivity analysis.

### equity-research-report
Laporan riset investasi bergaya sell-side (Goldman Sachs/Morgan Stanley/JPMorgan).

### equity-research-report-cn
Versi Chinese dari equity-research-report dengan CJK-first font strategy.

### earnings-review-note
Laporan review earnings sell-side (PDF/DOCX/PPTX) dengan EPS analysis dan variance tables.

### equity-earnings-review
Versi Chinese dari earnings-review-note.

### investment-memo
Structured investment analysis memo sebagai DOCX/PDF — VC deal memo dan thematic/macro memo.

### investor-letter-writer
Draft investment memo bergaya top VC deal memos atau investor letters.

### investor-pitch-planner
Structured fundraising pitch deck outlines dengan TAM/SAM/SOM market sizing.

### fundraising-bp-planner
Fundraising pitch deck outlines dengan 6 core modules dan data visualization recommendations.

### business-plan-ppt
PPT investment路演 dengan 14-section slide structure bergaya startup China.

### pitch-deck-creator
Professional pitch decks bergaya Chinese startup funding proposal.

### campaign-plan
Full campaign brief dengan objectives, audience, messaging, channel strategy, content calendar.

### campaign-planner
Versi Chinese dari campaign-plan dengan 10-chapter activity plan.

### churn-prevention
Churn reduction melalui cancel flow design, save offers, exit surveys, dan dunning sequences.

### retention-manager
SaaS churn prevention & retention strategies.

### pricing-advisor
Design/optimasi SaaS pricing systems dengan good-better-best tiers dan Van Westendorp analysis.

### pricing-strategy
Versi English dari pricing-advisor.

### saas-analyzer
SaaS business financial analysis — menghitung ARR, MRR, churn, LTV, CAC, NRR.

### saas-metrics-coach
Versi English dari saas-analyzer.

### split-test-evaluator
A/B testing analysis dengan Z-test, chi-square, confidence intervals, power analysis.

---

## 5. Writing & Content Creation Skills


### ad-copywriter
广告创意写作与优化（中文版），覆盖标题、描述、正文 untuk Google Ads, Meta, LinkedIn, TikTok, Twitter/X.

### ad-creative
English-language ad creative generation dan optimization untuk paid advertising platforms.

### audience-adapter
向上汇报与跨部门沟通助手中文版 dengan adaptasi otomatis ke CEO/VP/Tech Lead/Operations.

### audience-adaptive-comms
English-language stakeholder communication skill dengan 4 audience profiles.

### bloom-quiz-maker
Pembuat kuis berbasis Bloom's Taxonomy dengan 6 cognitive levels dan 3 tipe soal.

### content-research-writer
Penulisan konten berkualitas tinggi dengan research, citations, hooks, dan section-by-section feedback.

### copy-editing
Expert copy editor untuk marketing copy melalui 7 focused editing passes (English).

### copy-editor
Versi Chinese dari copy-editing dengan 七轮扫检框架.

### copywriting
Expert conversion copywriter untuk website pages (homepage, landing, pricing, feature, about).

### customer-reply-craft
客服话术生成器 untuk 4场景（售前/售后/投诉/退换货）dengan 5-level情绪安抚策略.

### ecom-copy-assistant
电商文案 untuk Taobao, JD.com, Amazon dengan platform-specific styles.

### ecom-listing-copywriter
Versi English dari ecom-copy-assistant.

### general-writing
Entry point untuk semua creative writing genres — fiction, poetry, lyrics, drama, screenplay, essay.

### humanizer
Removes AI-generated writing traces berdasarkan Wikipedia's "Signs of AI writing" guide.

### humanizer-zh
Versi Chinese dari humanizer dengan 5-dimension quality scoring system.

### humanizer-zh-by-guizang
Alternatif Chinese AI text humanizer berbasis hardikpandya/stop-slop.

### keynote-composer
Professional speech drafting dengan Aristotle's Rhetorical Triangle dan pause/tone annotations.

### longread
Penanganan file terlalu besar untuk single-pass reading dengan chunk-based parallel processing.

### marketing-writer
Penulisan/optimasi marketing copy untuk berbagai halaman fokus pada conversion rate.

### meeting-recap
Konversi meeting transcripts ke structured minutes dengan automatic action item extraction.

### structured-minutes
Structured meeting minutes dengan topic identification, decisions, dan action items.

### mock-interview-drill
Realistic mock interviews dengan follow-up drills untuk Behavioral, Technical, dan Case scenarios.

### interview-simulator
Interview simulator dengan 3-5 rounds progressive follow-ups dan STAR diagnosis.

### paper-review-coach
Simulasi academic peer review untuk kesiapan submission.

### podcast-blueprint
Podcast script generation dengan timestamps (Chinese).

### podcast-episode-writer
Podcast script generation dengan timestamps (English).

### pro-email-composer
Business email writing dengan tone calibration (Chinese/Bilingual).

### professional-email-composer
Business email writing (English counterpart).

### rhetoric-speech-craft
Professional speech drafting dengan annotations (Chinese).

### scholarly-writing-refiner
Polishing academic English writing paragraph by paragraph.

### short-video-script
Short video scripts untuk Douyin, TikTok, Reels dengan "3-second Hook → Conflict → Twist → CTA" structure.

### speech-synthesis
Text-to-speech menggunakan Microsoft Edge neural voice service.

### edge-tts
Text-to-speech dengan multiple languages, voices, adjustable speed/pitch.

### support-response-writer
Customer support replies dengan emotional de-escalation strategies.

### translation-craft
Chinese-English translation profesional dengan Faithfulness-Expressiveness-Elegance framework.

### xindaya-translator
Chinese-English bidirectional translation dengan 信达雅 principles dan back-translation verification.

### wechat-post-craft
WeChat Official Account article writing untuk viral articles.

### xhs-note-creator
小红书笔记创作工具 dengan title + body + tags + image card rendering.

### x-thread-crafter
Twitter/X threads dari long-form content dengan ≤280-character tweets.

### zhihu-viral-answer
知乎高赞回答 generator dengan story + substance + spark formula.

---

## 6. Coding & Development Skills


### backend-building
Backend skill dengan tRPC + Drizzle ORM + Hono — grafting ke webapp-building frontend.

### code-arch-optimizer
Codebase exploration untuk architectural improvement — deep refactoring proposals.

### code-mentor
Comprehensive AI programming tutor dengan 8 teaching modes untuk Python dan JavaScript.

### code-safety-audit
Security vulnerability scanning (Chinese) — dependency, secret leaks, OWASP anti-patterns.

### code-vuln-audit
Security vulnerability scanning (English) — sama dengan code-safety-audit.

### coding-discipline *(User Skill)*
Behavioral guardrails untuk coding tasks — 12 rules sebagai pre-flight checklist.

### conventional-commit-gen
Analisis git diff untuk generate Conventional Commits dengan auto scope detection.

### smart-commit-gen
规范化工具 untuk Conventional Commits dengan smart scope detection (Chinese).

### cross-examine
Relentless interviewing tentang plan/design sampai shared understanding tercapai.

### deep-module-refactor
Codebase exploration untuk architectural friction — shallow modules identification.

### dev-guide-generator
Complete technical tutorials via 8-phase SOP (English).

### dev-guide-writer
Complete technical tutorials via 8-phase SOP (Chinese).

### git-repo-audit
Deep analysis Git repository history — hot files, code ownership, secret leaks.

### gitlab-cli-guide
GitLab CLI (glab) reference dengan 30+ subcommands (Chinese).

### gitlab-cli-skills
GitLab CLI (glab) command reference (English).

### http-load-profiler
Stepped HTTP load testing dengan ab/wrk dan inflection point detection (English).

### http-load-tester
Stepped HTTP load testing (Chinese version).

### idea-to-prd
One-line requirement → complete PRD dengan user stories dan MoSCoW prioritization.

### interface-design-lab
Generate multiple fundamentally different interface designs melalui parallel exploration.

### api-shape-explorer
Generate multiple radically different API interface designs berdasarkan "Design It Twice" principle.

### iteration-planner
Agile Sprint planning assistant dengan capacity calculation dan load-balanced assignment.

### k8s-cluster-ops
Kubernetes cluster management via kubectl (Chinese).

### kubectl
Kubernetes cluster management via kubectl (English).

### landing-page-scaffold
Self-contained landing page HTML prototype dengan 5 sections.

### lp-proto-gen
One-click landing page HTML prototype generation.

### locale-guard
Frontend i18n/l10n setup, audit, dan enforcement (Chinese).

### localization-toolkit
Frontend i18n/l10n setup, audit, enforcement (English).

### log-diagnostic
Log file analysis untuk error pattern detection (Chinese).

### log-error-digest
Log file analysis untuk error pattern detection (English).

### outlier-scan
CSV anomaly detection menggunakan Z-score, IQR, dan moving average deviation.

### pipeline-blueprint
CI/CD best practices dan pipeline templates untuk GitHub Actions dan GitLab CI.

### programming-tutor
8-mode programming tutor (Chinese) untuk Python dan JavaScript.

### project-sizing-guide
Software project effort estimation dengan PERT, T-shirt sizing, FPA (English).

### workload-calculator
Software project effort estimation (Chinese) dengan three-point estimation.

### py-perf-analyzer
Python performance profiling — CPU, memory, line-by-line analysis (Chinese).

### regression-insight
OLS/Logit regression dengan Chinese interpretation.

### regression-modeler
OLS/Logit regression dengan English interpretation.

### repo-audit
Git hotspot/ownership/secret scanning (English).

### route-to-openapi
OpenAPI 3.0 spec generation dari code.

### rust-browser-pilot
Rust-based browser automation 10x faster than Puppeteer via Chrome DevTools Protocol.

### fast-browser-use
High-performance browser automation dengan DOM extraction dan anti-bot bypass.

### playwright-scraper-skill
Scraping dynamic websites menggunakan Playwright dengan stealth mode.

### smart-web-scraper
Playwright-based intelligent web scraper dengan anti-bot bypass.

### secure-code-review
Code security review berbasis OWASP Top 10 dengan remediation code.

### web-security-audit
Code security review (Chinese version) berbasis OWASP Top 10.

### seo-analyzer
Website SEO diagnosis dan optimization tool (Chinese).

### seo-audit
Website SEO audit tool (English).

### seo-content-writer
SEO content creation dengan 12-step workflow dan CORE-EEAT checklist.

### seo-copywriting-guide
SEO content creation (Chinese version).

### software-testing-guide
Comprehensive QA testing workflows dengan Google AAA-standard test cases.

### test-suite-architect
QA testing process dengan OWASP security coverage.

### sop-writer
SOP document generation dengan flowcharts, RACI matrices, dan detailed operation steps.

### process-doc
SOP/RACI/business process documentation (English).

### tdd-coach
TDD coaching dengan red-green-refactor loop (Chinese).

### test-driven-dev
TDD coaching dengan red-green-refactor loop (English).

### terraform-deploy-pitfalls
Terraform deployment operational traps dengan copy-paste fixes (English).

### terraform-deploy-traps
Terraform deployment pitfalls (Chinese version).

---

## 7. Financial & Trading Skills


### trading-education-doc *(User Skill)*
Membuat dokumen edukasi trading bergaya catatan markdown dengan timestamps `[HH:MM]`, structured sections, minimal styling.

### trading-alchemist-ebook *(User Skill)*
Membuat ebook edukasi trading bergaya visual "Trading Alchemist: New Edition" oleh Rizki Aditama — chapter-based dengan chart screenshots, flowcharts, summary boxes.

### trading-saham-bei *(User Skill)*
Membuat materi edukasi trading untuk Bursa Efek Indonesia (BEI/IDX) — strategy guides, stock analysis, trading psychology.

### stock-signal-analyzer
OHLCV technical indicator analysis (15+ indicators: MA, MACD, RSI, Bollinger Bands, KDJ).

### stock-tech-analysis
Versi Chinese dari stock-signal-analyzer.

### stock-finance-profiler
Stock fundamental analysis dengan 20+ financial indicators dan DuPont analysis.

### stock-research-report
Securities research reports bergaya Guotai Haitong / Haitong International.

### stock-research-report-cn
Versi Chinese dari stock-research-report.

### financial-ratio-toolkit
20+ financial ratios (profitability, solvency, liquidity, efficiency, growth) dan DuPont Analysis.

### financial-report-reader
Deep interpretation financial statements dengan YoY/QoQ analysis dan 10-dimension anomaly detection (Chinese).

### financial-statement-analyzer
Deep interpretation financial statements (English version).

### fund-risk-analyzer
ETF multi-dimensional comparison dengan annualized returns, max drawdown, Sharpe ratios (Chinese).

### fund-risk-compare
ETF multi-dimensional comparison (English version).

### value-invest-scorer
Buffett/Graham value investing assessment — 20 criteria across 4 dimensions (Chinese).

### value-investing-scorecard
Buffett/Graham value investing scorecard (English).

### cashflow-valuation
DCF现金流折现估值模型 dengan sensitivity analysis matrix (Chinese).

### discounted-cashflow-model
DCF valuation model dengan enterprise/equity/per-share value calculation.

---

## 8. Business & Marketing Skills


### brand-name-forge
Systematic brand naming workshop dengan 8 classic naming methods.

### brand-naming-lab
Versi Chinese dari brand-name-forge.

### cv-tailor
Resume optimization dengan JD keyword matching dan STAR method.

### resume-craft
Resume crafting dengan STAR & ATS checking (Chinese).

### work-recap-writer
Weekly/monthly report generation dari scattered notes dan git logs (English).

### work-report-writer
Weekly/monthly report generation (Chinese version).

### okr-planner
OKR creation/breakdown/retrospective coach (Chinese).

### okr-strategist
OKR drafting dan retrospective coach (English).

### email-manager
Send/receive/manage emails via IMAP/SMTP (Chinese).

### imap-smtp-email
Email management via IMAP dan SMTP (English).

### email-newsletter-builder
Professional HTML email newsletters compatible dengan Gmail, Outlook, Apple Mail.

### html-email-builder
HTML newsletters dengan table layouts dan inline CSS (Chinese).

### html-mail-builder
HTML email templates dengan 5 template types (Chinese).

### html-mailer-builder
HTML email templates dengan 5 template types (English).

### email-to-calendar
Calendar event extraction dari emails dengan duplicate detection.

### cross-platform-adapter
Content repurposing untuk LinkedIn, Twitter/X, WeChat, Zhihu, Slack.

---

## 9. Design & Visualization Skills


### baoyu-infographic
生成专业级信息图 dengan 21种版式 × 21种视觉风格.

### chart-gen
高质量PNG/SVG图表 dari JSON data（中文版）— 折线图、柱状图、面积图、K线图、饼图.

### chart-image
Publication-quality PNG charts dari data menggunakan Vega-Lite (English).

### chrono-flow
Beautiful interactive timeline HTML pages dari JSON data.

### timeline-builder
Interactive timeline HTML pages dengan vertical, horizontal, dual-side layouts.

### data-viz-gen
Self-contained HTML/SVG infographics dari JSON data — KPI stats, bar charts, flowcharts, dashboards.

### data-viz-renderer
Self-contained HTML/SVG infographics — same functionality.

### design-system-builder
Extract design systems dari reference UI images dan generate implementation-ready prompts.

### ui-blueprint
Extract design systems dari UI screenshots dan generate MVP UI prompts.

### fashion-sketch
Apparel technical specification packages (tech packs) dengan AI flat sketches dan fabric swatches (English).

### fashion-sketch-cn
Apparel tech packs (Chinese version).

### gantt-chart-builder
Interactive HTML Gantt charts dengan Critical Path Method analysis (Chinese).

### gantt-planner
Interactive HTML Gantt charts dengan CPM analysis (English).

### geo-magazine-slides
Geographic magazine-style PPTX presentations dengan editorial-quality layouts (English).

### geo-magazine-slides-cn
Geographic magazine-style PPTX presentations (Chinese).

### journalistic-portrait
Magazine-style HTML pages bergaya Southern People Weekly (English).

### journalistic-portrait-cn
Magazine-style HTML pages (Chinese).

### photo-magazine
Premium landscape documents dengan magazine-quality editorial design (English).

### photo-magazine-cn
Premium landscape documents (Chinese).

### retro-tech-illustration
Retro tech art generation (Synthwave, Cyberpunk, Vaporwave) — English.

### retro-tech-illustration-cn
Retro tech art generation (Chinese).

### risk-heatmap
Risk register dengan 5×5 probability-impact matrix (Chinese).

### theme-factory
Toolkit dengan 10 pre-set themes (colors dan fonts) — English.

### theme-kit
Toolkit dengan 10 pre-set themes (Chinese).

---

## 10. Data & Analytics Skills


### auto-hypothesis-test
Automated statistical testing — auto-selects t-test, ANOVA, chi-square, Mann-Whitney U, dll.

### auto-stat-test
Automated statistical testing (Chinese version).

### corr-insight
Pearson/Spearman correlation matrix, partial correlation, pseudo-correlation detection (Chinese).

### correlation-auditor
Pearson/Spearman correlation analysis (English version).

### database-inspector
SQLite/PostgreSQL database exploration dengan read-only queries dan Mermaid ER diagrams (Chinese).

### database-scout
SQLite/PostgreSQL database exploration (English version).

### dataset-health-audit
12-dimension data quality checks dengan scoring A+ sampai F (Chinese).

### dataset-quality-audit
12-dimension data quality audit (English version).

### ddd-glossary-gen
DDD-style ubiquitous language glossary extraction dari conversation (Chinese).

### domain-glossary
DDD ubiquitous language glossary (English version).

### outlier-scan
CSV anomaly detection dengan Z-score, IQR, moving average deviation.

### sql-insight
SQL query assistant — natural language to SQL, optimization, EXPLAIN interpretation (English).

### sql-tutor
SQL query assistant (Chinese version).

---

## 11. Communication & Productivity Skills


### adhd-assistant
ADHD-friendly life management — daily planning, task breakdown, time management, prioritization.

### adhd-daily-planner
ADHD life management (Chinese version).

### anki-card-maker
Flashcard generation dari study materials ke Anki-compatible CSV format.

### flashcard-studio
Flashcard extraction dan generation dengan spaced repetition principles.

### incident-retrospective
Blameless postmortem dengan 6-step SOP — timeline, 5 Whys, SMART actions (Chinese).

### incident-review-guide
Blameless postmortem (English version).

### iso-27001-evidence-collection
ISO 27001/SOC 2 audit evidence collection dan validation.

### legal-contract-gen
Legal document generation (NDA, service agreement, privacy policy) via interactive Q&A.

### legal-risk-analyzer
Legal risk assessment dengan severity × likelihood framework (Chinese).

### legal-risk-assessment
Legal risk assessment (English version).

### compliance-review-planner
Compliance checklists untuk GDPR, PIPL, Advertising Law, Data Security Law.

### regulatory-audit-generator
GDPR/PIPL compliance checklist builder.

### tos-clause-scanner
Terms of Service auditor untuk consumer risks — 7 risk categories.

### tos-risk-checker
ToS auditor (Chinese version).

### product-spec-writer
PRD generation dengan user stories dan MoSCoW prioritization.

### story-map-builder
Interactive HTML user story maps dengan Epic→Feature→Story structure.

### user-story-canvas
User story maps (Chinese version).

### weighted-scorer
Weighted scoring decision matrices untuk technology selection, vendor evaluation.

### weighted-scoring
Weighted scoring decision matrices (Chinese version).

### whatsapp-integration
WhatsApp messaging via Membrane CLI — text, image, video, document, template messages.

---

## 12. Security & Compliance Skills


### code-safety-audit
Security vulnerability scanning — dependency, secret leaks, OWASP (Chinese).

### code-vuln-audit
Security vulnerability scanning (English).

### secure-code-review
OWASP Top 10 code security review dengan remediation code.

### web-security-audit
OWASP-based code security review (Chinese).

### git-repo-audit
Git history analysis — hot files, ownership, secret leaks.

### terraform-deploy-pitfalls
Terraform deployment traps dan solutions (English).

### terraform-deploy-traps
Terraform deployment traps (Chinese).

### iso-27001-evidence-collection
ISO 27001/SOC 2 evidence collection.

### compliance-review-planner
Multi-regulation compliance checklists.

---

## 13. Specialized Domain Skills


### astro-observation-report
Gravitational-wave observational results papers untuk LIGO/Virgo/KAGRA (English).

### astro-observation-report-cn
Gravitational-wave papers (Chinese).

### sun-path
Sunlight dan shadow analysis untuk architectural design.

### sunlight-analysis
Sunlight analysis (Chinese version).

### video-compare-tool
Video compression quality comparison dengan PSNR/SSIM metrics.

### video-quality-diff
Video quality comparison dengan interactive HTML report.

### video-outline-planner
Bilibili video planning proposals untuk Knowledge, Lifestyle, Tech zones.

### scientific-problem-selection
Scientific problem selection framework berdasarkan Fischbach & Walsh (Cell, 2024).

### nuwa-by-huashu
Skill Creator — deep research, mental model extraction, character Skill generation.

---

## 14. Utility & Tool Skills


### browse
Browser automation via CLI — navigation, data extraction, screenshots.

### kimi-find-skills
Search dan discover skills across multiple sources (English).

### kimi-skills-finder
Search dan discover skills (Chinese).

### kimi-help-center
Kimi Product Help Center — routing questions ke correct articles.

### api-doc-gen
OpenAPI 3.0/Swagger generation dari Flask, FastAPI, Express, Gin code (Chinese).

### chart-gen
Chart generation dari JSON data (Chinese).

### chart-image
Chart generation (English version).

### code-to-chart
Code architecture diagrams via AST parsing ke Mermaid (Chinese).

### code-to-diagram
Code architecture diagrams (English version).

### data-viz-gen
HTML/SVG infographics generation.

### r2-upload
Cloudflare R2/S3 file upload dengan presigned URLs.

### speech-synthesis
Text-to-speech menggunakan Microsoft Edge neural voice.

---

## 15. User-Defined Skills


### trading-education-doc
Membuat dokumen edukasi trading dan transkripsi video dengan timestamps `[HH:MM]`, structured sections, minimal styling. Mendukung Indonesia dan English trading terminology.

### trading-alchemist-ebook
Membuat ebook edukasi trading bergaya visual "Trading Alchemist: New Edition" oleh Rizki Aditama. Chapter-based structure dengan chart screenshots, flowcharts, summary boxes, rich illustrations. Output: PDF (default) atau DOCX.

### trading-saham-bei
Membuat materi edukasi trading untuk Bursa Efek Indonesia (BEI/IDX) — swing trading, scalping, day trading guides, stock analysis reports, corporate actions, trading psychology, risk management, bit-offer analysis, tools screening guides.

### coding-discipline
Behavioral guardrails untuk coding tasks — 12 rules sebagai pre-flight checklist dan ongoing discipline. Mencegah overcomplication, hidden assumptions, unnecessary diffs, dan silent errors.

---

## 16. Struktur Direktori & Priority Rules


### Struktur Direktori

```
/app/.agents/skills/{skill_name}/SKILL.md     ← Built-in skills (260+ skills)
/app/.user/skills/{skill_name}/SKILL.md       ← User-defined skills
```

### Priority Rules
1. **User skill override** — Jika user skill dan built-in skill memiliki nama yang sama, **hanya user skill yang digunakan** (built-in skill diabaikan sepenuhnya)
2. **Progressive loading** — Skill hanya dibaca saat stage-nya tiba, tidak di-load semua di awal
3. **Composition** — Saat satu step membutuhkan Capability + Artifact skill, keduanya di-load. Jika konflik, Artifact Skill constraints menang

### Skill Categories Summary

| Kategori | Count | Contoh Utama |
|----------|-------|-------------|
| Deep Research | 4 | deep-research-swarm, deep-research, deep-probe, research-advisor |
| Report Writing | 3 | report-writing, paper-writing, general-writing |
| Web Development | 4 | vibecoding-webapp-swarm, vibecoding-general-swarm, webapp-building-swarm, webapp-building |
| SEO & Content | 20 | seo-analyzer, seo-audit, seo-content-writer, copywriting, copy-editing, humanizer, dll. |
| Finance & Investment | 28 | equity-research, stock-signal-analyzer, cashflow-valuation, fund-risk-analyzer, dll. |
| Data & Analytics | 16 | database-inspector, dataset-quality-audit, regression-modeler, outlier-scan, dll. |
| Security | 12 | code-safety-audit, secure-code-review, web-security-audit, terraform-deploy-pitfalls, dll. |
| Visualization | 18 | chart-gen, data-viz-gen, timeline-builder, gantt-chart-builder, baoyu-infographic, dll. |
| Communication | 22 | email-manager, meeting-recap, keynote-composer, interview-simulator, dll. |
| Specialized | 15 | astro-observation-report, sun-path, video-outline-planner, scientific-problem-selection, dll. |

---

> **Catatan:** Dokumentasi ini mencakup **260+ skill built-in** dan **4 user-defined skills** yang terdaftar dalam sistem Kimi K2.6 Agent Swarm. Setiap skill memiliki SKILL.md lengkap dengan instruksi, constraints, dan workflow patterns.
