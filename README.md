# Enterprise AI Orchestra

> Multi-domain AI orchestration için kavramsal mimari vision.
> Çoklu kanal · çoklu domain · federe veri · orkestra şefi + gruplar + enstrümanlar metaforu.

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Architecture%20Vision-blueviolet)](.)
[![Live Demo](https://img.shields.io/badge/Live-GitHub%20Pages-blue)](https://ibrahimsumbul.github.io/enterprise-ai-orchestra/)

Bu repo bir **kavramsal mimari vision** sunar — kod değil, fikir. Modern kurumsal AI'ın temel sorunu: tek tek akıllı araçlar **birlikte uyumlu** çalışmıyor. Bir orkestrayı orkestra yapan müzisyenler değil — **şef**.

## İki Görsel

| Doküman | Hedef kitle | Açıklama |
|---|---|---|
| [`orkestra-tanitim.html`](for-decision-makers/orkestra-tanitim.html) | Karar verici (CIO/CTO/operasyon yöneticisi) | 9 slayt, scroll-snap, klavye nav, light/dark mode auto, basıma uygun |
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
6. **KVKK/GDPR-grade audit** — sonradan eklenmiş özellik değil, mimarinin parçası
7. **Capability-based model routing** — domain reasoning Sonnet'te, retrieval/data Haiku'da

## Bu Repo **Ne Değil**?

- **Kod değil.** Implementation reference değil. (Hazır bir SaaS aramıyorsan, bu bir startup pitch'i değil.)
- **Müşteri-spesifik değil.** Generic kurumsal mimari, herhangi bir sektör/şirket adı yok.
- **Ürün belgesi değil.** Düşünce dokümanı + paylaşım için cilalı vision artifact.

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
**Toggle:** Diyagramda sağ üstte "Teknik detay" düğmesi — kavramsal/teknik versiyonu değiştir.

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
- **Çeviri** — özellikle İngilizce sürüm (mevcut Türkçe) için PR açık

Tasarım ilkelerinden birinde **farklı görüş**ün varsa Issue aç, tartışalım — pattern'ler eleştiriyle olgunlaşır.

## Lisans

[CC BY-SA 4.0](LICENSE) — paylaş, uyarla, ticari kullan; atıf ver + aynı lisansla paylaş.

Mimari vision dokümanları için CC-BY-SA klasik bir tercih: fikrin yayılmasını teşvik eder, türev eserlerin de aynı şekilde açık kalmasını şart koşar.

## Kim Yazdı?

**İbrahim Sümbül** · AI Systems Engineer · Hybrid AI Architectures · KVKK/GDPR-aware Enterprise AI

- GitHub: [github.com/ibrahimSumbul](https://github.com/ibrahimSumbul)
- LinkedIn: [linkedin.com/in/ibrahim-sümbül](https://www.linkedin.com/in/ibrahim-s%C3%BCmb%C3%BCl-838800300)
- Email: ibrahimsumbulll@gmail.com

> Bu pattern üzerine çalışan implementation **özel R&D**. Architecture deck ve engineering deep-dive talebe açık — iletişim için bağlantılar yukarıda.
