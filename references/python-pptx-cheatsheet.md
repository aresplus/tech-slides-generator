# Python-PPTX Anti-Hallucination & Syntax Guide

> **CRITICAL INSTRUCTION FOR CLAUDE**: 
> You MUST follow the exact syntax below. `python-pptx` does NOT support direct attribute assignment for many properties. Hallucinating methods will cause execution failure.

## 1. Setup & Constants
```python
from pptx import Presentation
from pptx.util import Inches, Pt
from pptx.dml.color import RGBColor
from pptx.enum.shapes import MSO_SHAPE
from pptx.enum.text import PP_ALIGN

# Use 16:9 template from assets
prs = Presentation('assets/base-template.pptx')