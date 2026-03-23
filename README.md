# FRET2WEST: Integration of FRET and WEST

🎉 **Welcome researchers!** This is the official companion repository for the published paper: _FRET2WEST: Exploring translation between temporal logic representations_.

## 📝 Publication & Citation

Our research has been published in the **Journal of Object Technology (JOT)** (Vol. 25, No. 1, 2026). If you utilize this framework or code in your research, please consider citing our work:

```bibtex
@article{lai2026fret2west,
  title={FRET2WEST: Exploring translation between temporal logic representations},
  author={Lai, Songyan and Monahan, Rosemary},
  journal={Journal of Object Technology},
  volume={25},
  number={1},
  pages={a2},
  year={2026}
}
```

---

## 🔍 Project Overview

This research originated as [Songyan Lai](https://songyanlai.github.io/)'s final year project for his undergraduate degree in Computer Science at the National University of Ireland Maynooth.

- **Authors**: Songyan Lai & Prof. Rosemary Monahan
- **Supervisor**: [Prof. Rosemary Monahan](https://www.maynoothuniversity.ie/faculty-science-engineering/our-people/rosemary-monahan)
- **Project Type**: Research & Tool Integration

---

## 🎯 Project Abstract

Software requirements are commonly expressed in natural-language, which must be formalised if they are to be used by formal methods to verify that an implementation abides by its requirements during execution. Tools such as the Formal Requirements Elicitation Tool (FRET) support this formalization, generating Linear Temporal Logic (LTL). However, development of safety-critical systems needs stringent requirements specification and verification across multiple tools.

This research accounts for syntactic and semantic differences between FRET and WEST, a tool that works with Mission-time LTL (MLTL) formulas to facilitate runtime verification via tools like R2U2. Our solution, **FRET2WEST**, utilizes regular expression-based mapping, variable normalization, and mission-time interval translation to transform FRET's LTL specifications to WEST's MLTL syntax. This translation is syntactically bridging and semantically preserving with bidirectional traceability to primal requirements. A proof-of-concept JavaScript translator, iteratively constructed through case studies, was incorporated as a feature within the MU-FRET tool. Comparative validation confirmed the efficacy of the framework, demonstrating enhanced reliability and efficiency in safety-critical requirements engineering.

For full details, please refer to the published paper or the original `Final Report.pdf` in this repository.

---

## 📂 Repository Structure

### FRET_to_WEST_MLTL_Converter

- **Code Implementation**: JavaScript/HTML syntax converter developed through ~10 iterations.
- **Testing Files**: Archive of iterative development artifacts.
- **Deployment Status**: Integrated into the [MU-FRET platform](https://github.com/valu3s-mu/mu-fret).

### Research_Documents

- **Key Analyses**:
  - _The Motivation for Integration of WEST and FRET_
  - _Exploring WEST's Role in Temporal Logic Validation_
- **Progress Reports**: Interim and Final Progress Reports.
- **Case Studies**:
  - Formal-to-Runtime Verification Pipeline Implementation
  - WEST Validation Compliance with R2U2 Monitoring Specifications
  - Applied Integration Patterns in Aerospace Systems
- **Supplementary Materials**: LTL Variants Survey, FRET/WEST comparative analysis, FRET-WEST-R2U2 Triad Study, and more.

---

## ✅ Completed Work

1. **Automated Translation Framework (FRET2WEST)**
   A JavaScript translator that resynchronizes FRET's LTL to WEST's MLTL, reducing manual translation time in industrial case studies. Innovations include Regex operator rewriting, finite-to-infinite trace emulation, and adaptive temporal granularity synchronization.
2. **Semantic-Preserving Heuristics**
   Problem-domain-specific rule sets maintain logical equivalence during conflicts in mission-time intervals and nesting operator alignment.
3. **Toolchain Interoperability**
   Mutual traceability provides linkages of MLTL results with FRETish requirements that are auditable and iteratively refineable.
4. **Empirical Validation**
   Case studies show 85% syntactic correctness and 80% semantic similarity between translated MLTL case studies and source FRET formulas.

---

## 🔮 Future Directions

1. **Semantic Equivalence Verification**: Integrate SMT solvers (e.g., Z3) to formally establish equivalence between FRET's LTL and MLTL translation.
2. **Multi-Tool Redundancy**: Expand integration to runtime monitors (e.g., R2U2) and probabilistic checkers (e.g., PRISM).
3. **Cloud-Native Scalability**: Execute containerized WEST instances on AWS/Azure for mission-scale verification.
4. **Human-Centric Interfaces**: Develop AI-enabled annotation tools to map validation errors back to FRETish requirements and enhance traceback in the GUI.

---

## 🔗 Collaborators & Acknowledgments

We extend our gratitude to the original NASA FRET development team and the WEST team for their foundational work, and to Oisin Sheridan (Maynooth University) and Zili Wang (Iowa State University) for their technical guidance and collaborative support.

_NASA Vision Statement: “To reach for new heights and reveal the unknown, so that what we do and learn will benefit all humankind.”_

- [NASA](https://www.nasa.gov/)
- [NASA FRET](https://github.com/NASA-SW-VnV/fret)
- [MU-FRET](https://github.com/valu3s-mu/mu-fret)
- [VALU3S](https://repo.valu3s.eu/)
- [WEST Tool](https://github.com/zwang271/WEST)

---

## 📚 Literature Review

1. **Temporal Logic Foundations**: Pnueli (1977) LTL → MLTL extensions (Rozier 2020)
2. **Verification Tools**: NASA FRET → MU-FRET safety adaptations
3. **WEST Validation**: Elwing et al. (2024) syntax flexibility analysis

_Last Updated: March 2026_  
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
