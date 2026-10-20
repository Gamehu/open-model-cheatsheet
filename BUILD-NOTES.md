# Build Notes — English public repo package

## Source

- Chinese source: `~/workspace/goals/open-model-selection-cheatsheet/files/open-model-cheatsheet/开源模型选型速查表.md`
- Source version: **v1.25**, data as of **2026-10-20**, 92 models covered, 124,382 bytes / 497 lines at build time
- Build date: 2026-10-20
- Pre-research followed: `hidden_files/english-public-repo/PROPOSAL.md` (terminology glossary, sample, license stance) and `README-draft.md`
- The Chinese source was **not** modified. No GitHub connection, no `git push` (not authorized).

## Translation conventions (binding for daily incremental translation)

1. **Glossary first.** All section names and column headers use the PROPOSAL glossary exactly, e.g.:
   开源模型选型速查表 = Open Model Cheatsheet; 快速选型（按场景）= Quick picks by scenario; 旗舰开源 LLM = Flagship open LLMs; 代码专用模型 = Code-specialized models; 小参数/端侧模型 = Small / edge models; 多模态理解 = Multimodal understanding; 语音（TTS / ASR）= Speech (TTS / ASR); 视频生成 = Video generation; 3D 生成 = 3D generation; 决策模型（typed-decision，新范式）= Decision models (typed-decision, emerging paradigm); 图像生成 = Image generation; 具身智能 / 世界动作模型 = Embodied AI / world-action models; 计算机使用（Computer-Use）Agent 模型 = Computer-use agent models; 结构化数据 / 表格基础模型 = Structured-data / tabular foundation models; 嵌入 / 检索模型 = Embedding / retrieval models; 时间序列 / 专项模型 = Time-series / specialized models; 榜单格局 = Benchmark landscape; Hugging Face 热榜快照 = Hugging Face trending snapshot; 监测中（暂不收录）= Watchlist (not yet listed); 许可风险提示 = License risk notes; 本地部署友好度排序 = Local-deployment friendliness ranking; 更新日志 = Changelog; 许可 = License; 擅长方向 = Strengths; 关键性能 = Key benchmarks; 大小 = Size; 本地部署 = Local deployment; 数据截至 = Data as of.
2. **Never translate:** model names, organization/repo ids, license names (MIT, Apache 2.0, OpenMDW-1.1, LFM Open License v1.0, StepFun Model License 1.0, Muse Model License, FLUX Kommunity License, Qwen Research License, CC BY-NC 4.0, etc.), benchmark names, numbers, dates, and URLs. Links are copied verbatim.
3. **Provenance tags on every score:** （官方）→ `(official)`, （第三方）→ `(third-party)`, 未核实 → `unverified`. Never drop, add, or upgrade a tag. 一手确认/核实 → "first-hand confirmed / first-hand verified".
4. **Version header alignment:** the English header line (`Version vX.Y · Data as of YYYY-MM-DD · …`) and the coverage count (92) must match the Chinese source of the same day, as must the README version line and "Last sync" date.
5. Vendor/attribution names in parentheses are translated descriptively where the source does so (阿里 = Alibaba, 腾讯 = Tencent, 智谱 = Zhipu, 月之暗面 = Moonshot AI, 深度求索 = DeepSeek, 面壁智能 = ModelBest, 上海AI实验室 = Shanghai AI Laboratory, 中国电信 = China Telecom); romanized product/org ids stay as-is.
6. ✅ / ⚠️ markers, table structure, row order, and appendix order are preserved 1:1 with the Chinese source.

## Notes for the daily sync cron (incremental translation)

- Translate **only the day's delta** from the sync notes (new rows, score updates, license changes, trending-snapshot replacement, new appendix recheck entries, new changelog entry); do not re-translate the whole file.
- The HF trending snapshot table is replaced wholesale each day — translate the new table (repo ids untranslated; 备注 column translated; ↑/↓/→/new markers kept).
- Appendix recheck entries are append-only and date-headed (`**YYYY-MM-DD recheck:**`) — translate and append in the same position/order as the Chinese source.
- Changelog: prepend the new version entry at the top of the Changelog list, keeping the exact version number and date of the Chinese source.
- If a Chinese entry says 未核实 / 口径冲突 / 待核实, the English must keep `unverified` (or "conflicting figures … unverified") — never smooth it over.
- After updating the English file, bump: (a) the English header version/data-date line, (b) `README.md` version line + "Last sync" date, in the same commit.
- License stance: this document is CC BY 4.0 (see `LICENSE`); model weights keep their own licenses — never restate a model's license in English differently from the Chinese source's verified wording, especially the "no LICENSE file in repo — verify before commercial use" caveats (TeleOCR, Ling-3.1-flash, MiniCPM-V-4.7).
