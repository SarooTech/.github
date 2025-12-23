# SarooTech Naming Principles (UIS Edition)

Unified naming convention integrating **Unified Identification System (UIS)** for global consistency across Git repos, Altium Designer, SolidWorks, C++, Python, folders, and files. **Hyphens (-) everywhere** as the universal separator. **No version numbers**—use Git for versioning (SemVer tags).

## Core Principles
- **All lowercase** except **UIS (ALL UPPERCASE)**
- **Hyphens (-)** only—no underscores, spaces, or special chars (< > : " \ | ? *)
- **UIS required** for: Git repos, root folders, **all CAD files**, **all Documents**
- **No UIS** for: code files (C++, Python) only
- **Max length**: Under 30 chars where possible

## SarooTech UIS Format
```
SAR-[D][T][G?][NNNN]
```
- **SAR**: SarooTech company code (UPPERCASE)
- **D**: Domain (1 char: P=Product, D=Document, S=Software, M=Mechanical)
- **T**: Type (1 char: E=Electronics, M=Mechanical, S=Software, D=Document)
- **G**: Group (1 char, optional: C=Component, A=Assembly, etc.)
- **NNNN**: Sequential 4-digit number (0001, 0002...)

## Correct UIS Examples (Core IDs Only)
```
SAR-PEC0001
SAR-MMC0002
SAR-DDO0003
SAR-SSW0004
```

## Naming by Context

### Git Repositories & Root Folders (UIS Required)
```
SAR-PEC0001-identification-system/
SAR-MMC0002-hardware-platform/
SAR-DDO0003-user-manual/
```

### Altium Designer (All Files: UIS Required)
```
SAR-PEC0001-identification-system.PrjPcb
SAR-PEC0001-mainboard.PcbDoc
SAR-PEC0002-connector.SchDoc
```

### SolidWorks (All Files: UIS Required)
```
SAR-MMC0001-enclosure.sldprt
SAR-MMC0002-chassis.sldasm
SAR-MMC0003-bracket.slddrw
```

### Documents (All Files: UIS Required)
```
SAR-DDO0001-api-reference.pdf
SAR-DDO0002-user-guide.md
SAR-DDO0003-test-report.docx
```

### C++ / Python (No UIS)
```
SAR-PEC0001-identification-system/           
├── src/
│   ├── id-generator.cpp
│   ├── config-manager.cpp
│   ├── api-handler.py
└── tests/
    ├── test-id-generator.cpp
    └── test-config.py
```

## Complete Project Example
```
SAR-PEC0001-identification-system/
├── SAR-PEC0001-identification-system.PrjPcb
│   ├── SAR-PEC0001-mainboard.PcbDoc
│   └── SAR-PEC0002-connector.SchDoc
├── SAR-MMC0001-enclosure.sldprt
├── SAR-DDO0001-api-reference.pdf
├── src/
│   ├── id-generator.cpp
│   └── config-manager.cpp
```

## Quick Rules Summary
| Context | UIS Required? | Pattern | Case | Separator |
|---------|---------------|---------|------|-----------|
| **Git Repos/Root** | ✅ | `SAR-[DTG][NNNN]-[purpose]` | UIS UPPER, purpose lower | Hyphen (-) |
| **CAD Files** | ✅ | `SAR-[DTG][NNNN]-[purpose].[ext]` | UIS UPPER, purpose lower | Hyphen (-) |
| **Documents** | ✅ | `SAR-DDO[NNNN]-[purpose].[ext]` | UIS UPPER, purpose lower | Hyphen (-) |
| **Code Files** | ❌ | `descriptive.ext` | All lower | Hyphen (-) |

## Why This Works
- **Visual Hierarchy**: `SAR-PEC0001-identification-system` (UPPER UIS + lower purpose)
- **Real-world Traceability**: Every physical/CAD/document artifact gets unique UIS
- **Clean Code**: Software files stay simple/readable
- **100% Hyphen Consistency** across all domains
- **Git Versioning**: `git tag v1.2.3`

**Rule**: **UIS (UPPERCASE) for all real-world/physical artifacts (CAD, docs). No UIS for pure software code files.**

*Last Updated: Dec 2025*[1]

[1](https://github.com/SarooTech)
