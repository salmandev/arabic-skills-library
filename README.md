# مكتبة المهارات العربية — Arabic Skills Library

> The first community-maintained collection of Arabic SKILL.md files for LLM agents

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Arabic First](https://img.shields.io/badge/Arabic-First-green.svg)](README.ar.md)
[![Validation](https://img.shields.io/badge/validation-automated-blue.svg)](docs/AUTOMATION.md)
[![Quality Gate](https://img.shields.io/badge/quality-gate-enabled-purple.svg)](docs/AUTOMATION.md)
[![Skills Count](https://img.shields.io/badge/skills-80+-red.svg)](docs/PROGRESS-TRACKER.md)

---

## 📖 Overview | نظرة عامة

**English**: `arabic-skills-library` is the first open-source collection of SKILL.md files designed specifically for Arabic-speaking developers building AI agents. This repository contains native Arabic instructions, bilingual templates, and MENA-specific compliance skills.

**العربية**: `مكتبة المهارات العربية` هي أول مجموعة مفتوحة المصدر من ملفات SKILL.md المصممة خصيصاً للمطورين الناطقين بالعربية الذين يبنون وكلاء الذكاء الاصطناعي. تحتوي هذه المستودع على تعليمات عربية أصيلة، وقوالب ثنائية اللغة، ومهارات امتثال خاصة بمنطقة الشرق الأوسط وشمال أفريقيا.

---

## 🎯 Why This Matters | الأهمية

| Statistic | English | العربية |
|-----------|---------|---------|
| Arabic speakers | 422M native speakers | ٤٢٢ مليون ناطق أصلي |
| Arabic SKILL.md coverage | <3% of public registries | أقل من ٣٪ من السجلات العامة |
| MENA compliance skills | Zero before this project | صفر قبل هذا المشروع |

### The Gap

- Arabic has **422 million native speakers** across 27 countries
- <3% of all SKILL.md files in public registries have any Arabic content
- Frameworks like LangChain and AutoGPT have **zero Arabic-adapted equivalents**
- Arabic LLM development (Falcon, JAIS, ALLaM, METABRAIN, Humain) is accelerating rapidly — but there are **no skills libraries** for developers building on them
- NCA ECC, SAMA CSF, PDPL — compliance frameworks unique to the region — have **no skill templates** anywhere
- Every MENA developer building AI agents is writing Arabic prompts from scratch, every single time

---

### Featured Skills

| Skill | Description | Language |
|-------|-------------|----------|
| [`nca-ecc-audit`](skills/government/nca-ecc-audit/SKILL.md) | Audit codebase against Saudi NCA ECC controls | Bilingual |
| [`sama-csf-review`](skills/government/sama-csf-review/SKILL.md) | SAMA Cybersecurity Framework compliance review | Bilingual |
| [`arabic-ml-model`](skills/developer/arabic-ml-model/SKILL.md) | Document ML models with Arabic explainability | Bilingual |
| [`arabic-ai-prompt`](skills/developer/arabic-ai-prompt/SKILL.md) | Master Arabic prompt engineering for LLMs | Bilingual |
| [`arabic-incident-response`](skills/security/arabic-incident-response/SKILL.md) | Incident response plans aligned with NCA ECC | Bilingual |
| [`arabic-medical-report`](skills/healthcare/arabic-medical-report/SKILL.md) | Write medical reports in formal Arabic | Arabic |
| [`arabic-email-drafter`](skills/business/arabic-email-drafter/SKILL.md) | Draft professional emails in formal Arabic | Arabic |
| [`arabic-proofreader`](skills/linguistics/arabic-proofreader/SKILL.md) | Proofread Arabic text for grammar and style | Arabic |
| [`rtl-css-skill`](skills/developer/rtl-css-skill/SKILL.md) | Generate RTL-compatible CSS for Arabic web apps | Bilingual |

---

## 🤖 Automation & Quality

This library uses comprehensive automation to maintain quality while scaling:

- ✅ **Automated Validation**: Every skill is validated for format, content, and quality
- ✅ **Quality Scoring**: Skills receive a quality grade (A+ to D)
- ✅ **CI/CD Pipeline**: GitHub Actions validate all changes automatically
- ✅ **PR Feedback**: Contributors receive instant feedback on their submissions

Learn more in our [Automation Documentation](docs/AUTOMATION.md)

### Quality Metrics

| Metric | Status | Target |
|--------|--------|--------|
| Total Skills | 80+ | 1000 |
| Validation Pass Rate | 95%+ | 98%+ |
| Average Quality Score | 82/100 | 85/100 |
| Arabic Content Ratio | 60%+ | 70%+ |

---

## 🚀 Quick Start | البدء السريع

### Install a Skill

```bash
# Using agency-agents-cli
agency-agents-cli install arabic-email-drafter --lang ar

# Or clone this repo
git clone https://github.com/arabic-skills-library/arabic-skills-library.git
```

### Use a Skill

1. Navigate to a skill directory (e.g., `skills/government/nca-ecc-audit/`)
2. Read the `SKILL.md` file
3. Copy the instructions into your LLM agent's system prompt
4. Trigger using the keywords listed in the skill

---

## 📁 Repository Structure | هيكل المستودع

```
arabic-skills-library/
├── README.md                          # You are here
├── README.ar.md                       # Full Arabic README
├── CONTRIBUTING.md                    # Volunteer guide (bilingual)
├── SKILL_TEMPLATE.md                  # Blank template for contributors
├── SKILL_TEMPLATE_BILINGUAL.md        # Bilingual template
├── skills/
│   ├── government/                    # حوكمة وامتثال
│   ├── education/                     # تعليم
│   ├── business/                      # أعمال
│   ├── developer/                     # أدوات المطورين
│   ├── healthcare/                    # صحة
│   ├── media/                         # إعلام ومحتوى
│   ├── security/                      # أمن وإدارة المخاطر
│   └── linguistics/                   # ترجمة ولغويات
├── dialects/
│   ├── gulf/                          # خليجي
│   ├── levantine/                     # شامي
│   └── egyptian/                      # مصري
├── llm-compatibility/                 # LLM-specific notes
├── tools/                             # CLI utilities
├── docs/                              # Documentation
└── .github/                           # GitHub templates & workflows
```

---

## 🤝 Contributing | المساهمة

We welcome volunteers! See [CONTRIBUTING.md](CONTRIBUTING.md) for:

- How to contribute a skill
- Quality standards
- Volunteer badges and recognition
- Priority skill requests

### Priority Requests (CRITICAL 🔴)

1. NCA ECC & SAMA CSF compliance skills (Riyadh/KSA context)
2. Arabic medical report templates
3. Gulf dialect variants for existing English skills
4. Arabic RTL CSS/UI skills for developers

---

## 📜 License | الترخيص

MIT License — See [LICENSE](LICENSE) for details.

---

## 🌟 Contributors | المساهمون

<!-- markdownlint-disable-next-line -->
<table>
  <tr>
    <td align="center">
      <strong>Founding Contributor</strong><br/>
      Salman Shaikh
    </td>
  </tr>
</table>

---

## 📬 Contact | التواصل

- **GitHub Issues**: [Report a bug or request a skill](https://github.com/arabic-skills-library/arabic-skills-library/issues)
- **SkillForge Registry**: Skills auto-submitted to SkillForge under category "Arabic/MENA"

---

<div align="center">

**Built with ❤️ for the Arabic-speaking developer community**

صُنع بحب ❤️ لمجتمع المطورين الناطقين بالعربية

</div>
