# MedGamma
# MedGemma Multimodal Clinical Report Generator 🩺🤖

An end-to-end, memory-optimized AI pipeline that leverages Google's **MedGemma 3 (4-bit quantized)** vision-language model to analyze visual medical scans (e.g., PET scans, X-rays) using multi-shot in-context learning, automatically generating highly structured, publication-quality diagnostic reports in PDF format.

---

## 🚀 Key Features

* **Advanced Multi-Shot Prompting:** Utilizes Hugging Face's native `.apply_chat_template()` processing logic to dynamically inject multi-image historical examples into the conversation buffer, preventing token mismatching.
* **4-Bit Quantization Optimization:** Built using `bitsandbytes` (NF4 quantization scheme) and `accelerate` to drastically lower the VRAM footprint, allowing a powerful medical visual-language model to run efficiently on accessible consumer hardware like a free T4 cloud GPU.
* **Automated PDF Compilation Architecture:** Bypasses basic text output formatting by integrating the `weasyprint` layout engine, translating raw clinical text outputs into highly structured HTML/CSS stylized documents ready for professional printing.
* **Cloud Storage Pipeline Integration:** Features an absolute directory management scheme to autonomously save, organize, and timestamp generated medical logs across cloud workspace nodes.

---

## 🛠️ Repository Architecture

```text
📁 medgemma-scan-analyzer/
│
├── 📄 main.py                   # Self-contained pipeline execution logic
├── 📄 perfect_templates.json     # Sample multi-shot context dataset template
├── 📄 requirements.txt          # Production environment package checklist
└── 📄 README.md                 # Project documentation & presentation page
