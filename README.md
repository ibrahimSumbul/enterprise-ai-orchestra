# Enterprise AI Orchestra

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Architecture%20Vision-blueviolet)](.)
[![Live Demo](https://img.shields.io/badge/Live-GitHub%20Pages-blue)](https://ibrahimsumbul.github.io/enterprise-ai-orchestra/)

<sub>🌐 **Türkçe** · [English](#english)</sub>

> Multi-domain AI orchestration için kavramsal mimari vision.
> Çoklu kanal · çoklu domain · federe veri · orkestra şefi + gruplar + enstrümanlar metaforu.

Bu repo bir **kavramsal mimari vision** sunar — kod değil, fikir. Modern kurumsal AI'ın asıl sorunu şu: tek tek akıllı araçlar **birlikte uyum içinde** çalışmıyor. Bir orkestrayı orkestra yapan müzisyenler değil — **şef**.

> **Public-safe not:** Bu çalışma kişisel olarak hazırlanmış, vendor-neutral bir referans mimaridir. Herhangi bir şirket verisi, iç sistem detayı, müşteri bilgisi veya kuruma özel implementation bilgisi içermez.

## İki Görsel

| Doküman | Hedef kitle | Açıklama |
|---|---|---|
| [`orkestra-tanitim.html`](for-decision-makers/orkestra-tanitim.html) | Karar verici (CIO/CTO/operasyon yöneticisi) | 9 slayt, scroll-snap, klavye nav, açık/koyu tema (oto + manuel), basıma uygun |
| [`orkestra-diagram.html`](for-decision-makers/orkestra-diagram.html) | Mimari okuyucu | Tek bakışta interaktif harita, collapsible katman bilgisi, teknik detay toggle |

**Canlı:** https://ibrahimsumbul.github.io/enterprise-ai-orchestra/

## 4 Katmanlı Yapı

Bu repo, "agentic orchestration" üzerine kapsamlı bir mimari deseni görselleştirir:

| # | Katman | Sorumluluk |
|---|---|---|
| 1 | **Kanallar** | Dashboard, sohbet (WhatsApp/Teams/web), proaktif bildirim — kullanıcının dokunduğu yüz |
| 2 | **Orkestra Şefi** | Intent routing, hafıza (Continuum), yetki/guardrails, denetim kaydı, onay kuyruğu |
| 3 | **Gruplar** | İK, Satın alma, Lojistik, Finans, Üretim, Müşteri Hizmetleri, ... (domain agents) |
| 4 | **Enstrümanlar** | Mevcut kurumsal sistemler (ERP, CRM, DMS, envanter, Graph API) — **federe**, yerinde kalır, ETL yok |

## Tasarım İlkeleri

1. **Federe veri** — kaynaklar yerinde kalır, soru anında çağrılır, ETL/ambar yok
2. **Boundary Agent Doctrine** — sistem sınırını aşan her capability bir agent'la sarılır; pure function direkt çağrılır
3. **Üç tip agent** — Domain (Sonnet) · Horizontal (Haiku) · Data-Layer (Haiku + MCP server)
4. **Dört protokol** — Direct tool · MCP · A2A · Service call
5. **Continuum** — Memory + Mediator unified (cross-channel coordination, tek modül)
6. **KVKK/GDPR-aware auditability** — sonradan eklenmiş özellik değil, mimarinin parçası
7. **Capability-based model routing** — domain reasoning Sonnet'te, retrieval/data Haiku'da

## Bu Repo **Ne Değil**?

- **Kod değil.** Implementation reference değil. (Hazır bir SaaS aramıyorsan, bu bir startup pitch'i değil.)
- **Müşteri-spesifik değil.** Generic kurumsal mimari, herhangi bir sektör/şirket adı yok.
- **Ürün belgesi değil.** Düşünce dokümanı + paylaşım için cilalı vision artifact.
- **Kuruma özel uygulama detayı içermez.** Gerçek şirket verisi, iç sistem adı, entegrasyon detayı veya operasyonel bilgi paylaşılmaz.

## Hızlı Başlangıç

```bash
# Lokal aç
git clone https://github.com/ibrahimSumbul/enterprise-ai-orchestra.git
cd enterprise-ai-orchestra
open index.html  # macOS — landing page
# veya doğrudan:
open for-decision-makers/orkestra-tanitim.html
```

**Klavye:** `↑` `↓` slayt gez (tanıtım), `P` yazdır, `space` ilerle.
**Teknik toggle:** Diyagramda sağ üstte "Teknik detay" düğmesi — kavramsal/teknik versiyonu değiştir.
**Dil:** Her sayfada üst köşede `TR | EN` düğmesi — seçim hatırlanır ve `?lang=en` ile paylaşılabilir; ilk ziyarette tarayıcı diline göre otomatik açılır.
**Tema:** Tanıtım sayfasında sağ üstte ☀️/🌙 düğmesi — açık/koyu tema; seçim hatırlanır, ilk ziyarette sistem tercihine uyar.

## Yapı

```
enterprise-ai-orchestra/
├── README.md
├── LICENSE              # CC BY-SA 4.0
├── index.html           # Landing — iki HTML'e yönlendirir
├── .nojekyll            # GitHub Pages Jekyll bypass
└── for-decision-makers/
    ├── orkestra-tanitim.html    # 9 slayt sunum
    └── orkestra-diagram.html    # tek bakışta interaktif harita
```

## Katkı

Bu kavramsal bir vision. Geri bildirim hoş karşılanır:

- **Mimari soru veya öneri** — [GitHub Issues](https://github.com/ibrahimSumbul/enterprise-ai-orchestra/issues)
- **Yazım/dil düzeltmesi** — direkt PR
- **Çeviri** — Türkçe ve İngilizce birlikte tutuluyor; her ikisini iyileştiren PR'lar açık

Tasarım ilkelerinden birine **katılmıyorsan** Issue aç, tartışalım — desenler eleştiriyle olgunlaşır.

## Lisans

[CC BY-SA 4.0](LICENSE) — paylaş, uyarla, ticari kullan; atıf ver + aynı lisansla paylaş.

Mimari vision dokümanları için CC-BY-SA klasik bir tercih: fikrin yayılmasını teşvik eder, türev eserlerin de aynı şekilde açık kalmasını şart koşar.

## Kim Yazdı?

**İbrahim Sümbül** · AI Systems Engineer · Hybrid AI Architectures · KVKK/GDPR-aware Enterprise AI

- GitHub: [github.com/ibrahimSumbul](https://github.com/ibrahimSumbul)
- LinkedIn: [linkedin.com/in/ibrahim-sümbül](https://www.linkedin.com/in/ibrahim-s%C3%BCmb%C3%BCl-838800300)
- Email: ibrahimsumbulll@gmail.com

> Bu pattern üzerine private implementation keşifleri ayrı yürütülür; public repo yalnızca generic mimari yaklaşımı ve sistem tasarımı kapsamını paylaşır. Architecture deck ve engineering deep-dive talebe açık — iletişim için bağlantılar yukarıda.

---

# English

<sub>[Türkçe ↑](#enterprise-ai-orchestra) · 🌐 **English**</sub>

> A conceptual architecture vision for multi-domain AI orchestration.
> Multi-channel · multi-domain · federated data · conductor + sections + instruments metaphor.

This repo presents a **conceptual architecture vision** — an idea, not code. The core problem of modern enterprise AI: individually smart tools don't work **in harmony**. What makes an orchestra an orchestra isn't the musicians — it's the **conductor**.

> **Public-safe note:** This is a personally authored, vendor-neutral reference architecture. It contains no company data, internal system detail, customer information, or organization-specific implementation knowledge.

## Two Visuals

| Document | Audience | Description |
|---|---|---|
| [`orkestra-tanitim.html`](for-decision-makers/orkestra-tanitim.html) | Decision-maker (CIO/CTO/operations lead) | 9 slides, scroll-snap, keyboard nav, light/dark mode (auto + manual), print-friendly |
| [`orkestra-diagram.html`](for-decision-makers/orkestra-diagram.html) | Architecture reader | Interactive map at a glance, collapsible layer info, technical-detail toggle |

**Live:** https://ibrahimsumbul.github.io/enterprise-ai-orchestra/

## The Four-Layer Structure

This repo visualizes a comprehensive architectural pattern for "agentic orchestration":

| # | Layer | Responsibility |
|---|---|---|
| 1 | **Channels** | Dashboard, chat (WhatsApp/Teams/web), proactive notifications — the surface the user touches |
| 2 | **Conductor** | Intent routing, memory (Continuum), permissions/guardrails, audit trail, approval queue |
| 3 | **Sections** | HR, Procurement, Logistics, Finance, Production, Customer Service, ... (domain agents) |
| 4 | **Instruments** | Existing enterprise systems (ERP, CRM, DMS, inventory, Graph API) — **federated**, stay in place, no ETL |

## Design Principles

1. **Federated data** — sources stay in place, called at query time, no ETL/warehouse
2. **Boundary Agent Doctrine** — every capability that crosses a system boundary is wrapped in an agent; pure functions are called directly
3. **Three agent types** — Domain (Sonnet) · Horizontal (Haiku) · Data-Layer (Haiku + MCP server)
4. **Four protocols** — Direct tool · MCP · A2A · Service call
5. **Continuum** — Memory + Mediator unified (cross-channel coordination, one module)
6. **KVKK/GDPR-aware auditability** — not a bolt-on, part of the architecture
7. **Capability-based model routing** — domain reasoning on Sonnet, retrieval/data on Haiku

## What This Repo Is **Not**

- **Not code.** Not an implementation reference. (This isn't a startup pitch, and it isn't a ready-made SaaS.)
- **Not customer-specific.** A generic enterprise architecture; no industry or company names.
- **Not product documentation.** A thinking document — a polished vision artifact meant to be shared.
- **Contains no organization-specific implementation detail.** No real company data, internal system names, integration details, or operational information is shared.

## Quick Start

```bash
# Open locally
git clone https://github.com/ibrahimSumbul/enterprise-ai-orchestra.git
cd enterprise-ai-orchestra
open index.html  # macOS — landing page
# or directly:
open for-decision-makers/orkestra-tanitim.html
```

**Keyboard:** `↑` `↓` move between slides (deck), `P` print, `space` advance.
**Technical toggle:** the "Technical detail" button at the top right of the diagram — switch between the conceptual and technical versions.
**Language:** every page has a `TR | EN` button in the top corner — the choice is remembered and shareable via `?lang=en`; on first visit it follows the browser language automatically.
**Theme:** the deck has a ☀️/🌙 button at the top right — light/dark; the choice is remembered and follows the system preference on first visit.

## Structure

```
enterprise-ai-orchestra/
├── README.md
├── LICENSE              # CC BY-SA 4.0
├── index.html           # Landing — links to the two HTML files
├── .nojekyll            # GitHub Pages Jekyll bypass
└── for-decision-makers/
    ├── orkestra-tanitim.html    # 9-slide deck
    └── orkestra-diagram.html    # interactive map at a glance
```

## Contributing

This is a conceptual vision. Feedback is welcome:

- **Architecture questions or suggestions** — [GitHub Issues](https://github.com/ibrahimSumbul/enterprise-ai-orchestra/issues)
- **Typos / wording fixes** — open a PR directly
- **Translations** — both Turkish and English are maintained; PRs improving either are welcome

If you disagree with one of the design principles, open an Issue and let's discuss — patterns mature through critique.

## License

[CC BY-SA 4.0](LICENSE) — share, adapt, use commercially; give attribution + share alike.

CC-BY-SA is a classic choice for architecture-vision documents: it encourages the idea to spread while requiring derivative works to stay equally open.

## Who Wrote This?

**İbrahim Sümbül** · AI Systems Engineer · Hybrid AI Architectures · KVKK/GDPR-aware Enterprise AI

- GitHub: [github.com/ibrahimSumbul](https://github.com/ibrahimSumbul)
- LinkedIn: [linkedin.com/in/ibrahim-sümbül](https://www.linkedin.com/in/ibrahim-s%C3%BCmb%C3%BCl-838800300)
- Email: ibrahimsumbulll@gmail.com

> Private implementation explorations of this pattern are pursued separately; the public repo shares only the generic architectural approach and system-design scope. Architecture deck and engineering deep-dive available on request — contact links above.
