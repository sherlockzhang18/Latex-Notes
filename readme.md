# LaTeX Notes Workspace

This repository contains a comprehensive collection of LaTeX notes for various mathematics and computer science courses. The workspace is optimized for efficient LaTeX development with automated building and extensive snippet support.

## 📁 Repository Structure

```
├── Archive/                 # Archived course notes
│   ├── CSE_3407/           # Computer Science course
│   ├── Math_4150/          # Mathematics course
│   └── Math_4351/          # Mathematics course
├── CSE_4102/               # Current Computer Science course
├── Math_4301/              # Current Mathematics course
├── Math_4501/              # Current Mathematics course
├── template/               # Template files for new courses
│   ├── les_01.tex          # Lesson template
│   ├── master.tex          # Master document template
│   ├── preamble.tex        # Common preamble template
│   └── hw/                 # Homework templates
└── .vscode/                # VS Code configuration
    └── settings.json       # LaTeX Workshop settings and snippets
```

## 🛠️ Workspace Setup

### Prerequisites

1. **Git** - For cloning the repository
2. **LaTeX Distribution** - TeX Live (recommended) or MiKTeX
3. **VS Code** - Recommended IDE
4. **latexmk** - Automated LaTeX building tool

### Installation Steps

#### 1. Clone the Repository

```bash
git clone https://github.com/sherlockzhang18/Latex-Notes.git
cd Latex-Notes
```

#### 2. Install LaTeX Distribution

**macOS (using Homebrew):**
```bash
brew install --cask mactex
```

**Ubuntu/Debian:**
```bash
sudo apt update
sudo apt install texlive-full
```

**Windows:**
Download and install MiKTeX from [miktex.org](https://miktex.org/download)

#### 3. Install latexmk

latexmk is usually included with TeX Live. If not installed:

**macOS/Linux:**
```bash
# Usually comes with texlive-full
# If missing, install separately:
sudo apt install latexmk  # Ubuntu/Debian
brew install latexmk      # macOS
```

**Windows:**
latexmk comes with MiKTeX installation.

#### 4. Setup VS Code

1. **Install VS Code** from [code.visualstudio.com](https://code.visualstudio.com/)

2. **Install LaTeX Workshop Extension:**
   - Open VS Code
   - Go to Extensions (Ctrl+Shift+X)
   - Search for "LaTeX Workshop"
   - Install the extension by James Yu

3. **Import Workspace Settings:**
   - Open the cloned repository in VS Code
   - The `.vscode/settings.json` file will automatically configure:
     - Auto-build on save
     - LaTeX tools and recipes
     - File cleaning settings
     - Extensive snippet library
     - Syntax highlighting and IntelliSense

### 🎯 VS Code Configuration Features

The included `settings.json` provides:

#### **Build Automation:**
- Auto-build on file save
- Uses latexmk with synctex support
- Automatic cleanup of auxiliary files
- PDF generation with error handling

#### **Enhanced Snippets:**
- **TikZ Graphics:** `tikz`, `tikzpicture`, `draw`, `fill`, `node`
- **Figures:** `figure`, `figures` (side-by-side)
- **Tables:** `table` with customizable structure
- **Lists:** `enumerate`, `itemize`
- **Algorithms:** `algorithm`, `algorithmic`
- **Charts:** PGFPlots templates for data visualization

#### **Development Tools:**
- Syntax error highlighting
- PDF preview with SyncTeX
- Context menu integration
- Package IntelliSense

### 📝 Usage

1. **Start a New Course:**
   ```bash
   cp -r template/ NewCourse_XXXX/
   cd NewCourse_XXXX/
   # Edit master.tex and preamble.tex as needed
   ```

2. **Create New Lesson:**
   ```bash
   cp les_01.tex les_XX.tex
   # Edit lesson content
   # Add \input{les_XX} to master.tex
   ```

3. **Build Documents:**
   - Save any `.tex` file to trigger auto-build
   - PDF will be generated in the same directory
   - Use Ctrl+Alt+B for manual build

4. **Use Snippets:**
   - Type snippet prefix (e.g., `tikz`, `figure`, `table`)
   - Press Tab to expand
   - Navigate through placeholders with Tab

### 🔧 Customization

#### Adding New Snippets:
Edit `.vscode/settings.json` and add new snippet definitions following the existing pattern.

#### Modifying Build Settings:
Adjust the `latex-workshop.latex.tools` and `latex-workshop.latex.recipes` sections in settings.json.

### 📚 Course Structure

Each course directory follows this pattern:
- `master.tex` - Main document that includes all lessons
- `preamble.tex` - Common packages and custom commands
- `les_XX.tex` - Individual lesson files
- `hw/` - Homework assignments (when applicable)

### 🤝 Contributing

1. Create feature branches for new courses or major changes
2. Follow the existing directory structure
3. Update templates when adding new common patterns
4. Test build process before committing

### 📄 License

This repository contains academic notes and is intended for educational purposes.