# Custom Key-mappings

Note that,

* **Leader** key set as <kbd>Space</kbd>
* **Local-Leader** key set as <kbd>;</kbd> and used for navigation and search
  (Denite and Defx)
* Disable <kbd>←</kbd> <kbd>↑</kbd> <kbd>→</kbd> <kbd>↓</kbd> in normal mode by enabling `g:elite_mode` in `.vault.vim`

<details open>
  <summary>
    <strong>Key-mappings</strong>
    <small><i>(🔎 Click to expand/collapse)</i></small>
  </summary>

<center>Modes: 𝐍=normal 𝐕=visual 𝐒=select 𝐈=insert 𝐂=command</center>

### Navigation

| Key   | Mode | Action             | Plugin or Mapping
| ----- |:----:| ------------------ | ------
| <kbd>j</kbd> / <kbd>k</kbd> | 𝐍 𝐕 | Cursor moves through display-lines | `g` `j/k`
| <kbd>g</kbd>+<kbd>j</kbd> / <kbd>k</kbd> | 𝐍 𝐕 𝐒 | Jump to edge upward/downward | <small>[haya14busa/vim-edgemotion]</small>
| <kbd>gh</kbd> / <kbd>gl</kbd> | 𝐍 𝐕 | Easier line-wise movement | `g` `^/$`
| <kbd>Space</kbd>+<kbd>Space</kbd> | 𝐍 𝐕 | Toggle visual-line mode | `V` / <kbd>Escape</kbd>
| <kbd>v</kbd> / <kbd>V</kbd> | 𝐕 | Expand/reduce selection | <small>[terryma/vim-expand-region]</small>
| <kbd>zl</kbd> / <kbd>zh</kbd> | 𝐍 | Scroll horizontally and vertically wider | `z4` `l/h`
| <kbd>Ctrl</kbd>+<kbd>j</kbd> | 𝐍 | Move to split below | <small>[christoomey/tmux-navigator]</small>
| <kbd>Ctrl</kbd>+<kbd>k</kbd> | 𝐍 | Move to upper split | <small>[christoomey/tmux-navigator]</small>
| <kbd>Ctrl</kbd>+<kbd>h</kbd> | 𝐍 | Move to left split | <small>[christoomey/tmux-navigator]</small>
| <kbd>Ctrl</kbd>+<kbd>l</kbd> | 𝐍 | Move to right split | <small>[christoomey/tmux-navigator]</small>
| <kbd>Return</kbd> | 𝐍 | Toggle fold | `za`
| <kbd>Shift</kbd>+<kbd>Return</kbd> | 𝐍 | Focus the current fold by closing all others | `zMzvzt`
| <kbd>]q</kbd> or <kbd>]q</kbd> | 𝐍 | Next/previous on quickfix list | `:cnext` / `:cprev`
| <kbd>]l</kbd> or <kbd>]l</kbd> | 𝐍 | Next/previous on location-list | `:lnext` / `:lprev`
| <kbd>]w</kbd> or <kbd>]w</kbd> | 𝐍 | Next/previous whitespace error | <small>[plugin/whitespace.vim]</small>
| <kbd>]g</kbd> or <kbd>]g</kbd> | 𝐍 | Next/previous Git hunk | <small>[airblade/vim-gitgutter]</small>
| <kbd>]d</kbd> or <kbd>]d</kbd> | 𝐍 | Next/previous LSP diagnostic | <small>[mattn/vim-lsp-settings]</small>
| <kbd>Ctrl</kbd>+<kbd>f</kbd> | 𝐂 | Move cursor forwards in command | <kbd>Right</kbd>
| <kbd>Ctrl</kbd>+<kbd>b</kbd> | 𝐂 | Move cursor backwards in command | <kbd>Left</kbd>
| <kbd>Ctrl</kbd>+<kbd>h</kbd> | 𝐂 | Move cursor to the beginning in command | <kbd>Home</kbd>
| <kbd>Ctrl</kbd>+<kbd>l</kbd> | 𝐂 | Move cursor to the end in command | <kbd>End</kbd>

### File Operations

| Key   | Mode | Action             | Plugin or Mapping
| ----- |:----:| ------------------ | ------
| <kbd>Space</kbd>+<kbd>cd</kbd> | 𝐍 | Switch to the directory of opened buffer | `:lcd %:p:h`
| <kbd>gf</kbd> | 𝐍 𝐕 | Open file under the cursor in a vsplit | `:rightbelow wincmd f`
| <kbd>Space</kbd>+<kbd>w</kbd> | 𝐍 𝐕 𝐒 | Write buffer to file | `:write`
| <kbd>Ctrl</kbd>+<kbd>s</kbd> | 𝐍 𝐕 𝐒 𝐂 | Write buffer to file | `:write`

### Edit

| Key   | Mode | Action             | Plugin or Mapping
| ----- |:----:| ------------------ | ------
| <kbd>Ctrl</kbd>+<kbd>Return</kbd> | 𝐈 | Expand emmet abbreviation | <small>[mattn/emmet-vim]</small>
| <kbd>Q</kbd> | 𝐍 | Start/stop macro recording | `q`
| <kbd>gQ</kbd> | 𝐍 | Play macro 'q' | `@q`
| <kbd>Shift</kbd>+<kbd>Return</kbd> | 𝐈 | Start new line from any cursor position | `<C-o>o`
| <kbd><</kbd> | 𝐕 𝐒 | Indent to left and re-select | `<gv`
| <kbd>></kbd> | 𝐕 𝐒 | Indent to right and re-select | `>gv|`
| <kbd>Tab</kbd> | 𝐕 𝐒 | Indent to right and re-select | `>gv|`
| <kbd>Shift</kbd>+<kbd>Tab</kbd> | 𝐕 𝐒 | Indent to left and re-select | `<gv`
| <kbd>gc</kbd> | 𝐍 𝐕 𝐒 | Caw (comments plugin) prefix | <small>[tyru/caw.vim]</small>
| <kbd>gcc</kbd> | 𝐍 𝐕 𝐒 | Toggle comments | <small>[tyru/caw.vim]</small>
| <kbd>Space</kbd>+<kbd>v</kbd> | 𝐍 𝐕 𝐒 | Toggle single-line comments | <small>[tyru/caw.vim]</small>
| <kbd>Space</kbd>+<kbd>V</kbd> | 𝐍 𝐕 𝐒 | Toggle comment block | <small>[tyru/caw.vim]</small>
| <kbd>Space</kbd>+<kbd>j</kbd> or <kbd>k</kbd> | 𝐍 𝐕 | Move lines down/up | `:m` …
| <kbd>Space</kbd>+<kbd>d</kbd> | 𝐍 𝐕 | Duplicate line or selection |
| <kbd>Space</kbd>+<kbd>cn</kbd> / <kbd>cN</kbd> | 𝐍 𝐕 | Change current word in a repeatable manner |
| <kbd>Space</kbd>+<kbd>cp</kbd> | 𝐍 | Duplicate paragraph | `yap<S-}>p`
| <kbd>Space</kbd>+<kbd>cw</kbd> | 𝐍 | Remove all spaces at EOL | `:%s/\s\+$//e`
| <kbd>Ctrl</kbd>+<kbd>g</kbd> <kbd>g</kbd> | 𝐈 | Jump outside of pair | <small>[Raimondi/delimitMate]</small>
| <kbd>sj</kbd> / <kbd>sk</kbd> | 𝐍 | Join/split arguments | <small>[AndrewRadev/splitjoin.vim]</small>
| <kbd>dsf</kbd> / <kbd>csf</kbd> | 𝐍 | Delete/change surrounding function call | <small>[AndrewRadev/dsf.vim]</small>

### Search & Replace

| Key   | Mode | Action             | Plugin or Mapping
| ----- |:----:| ------------------ | ------
| <kbd>Space</kbd>+<kbd>f</kbd> | 𝐍 | Filter lines in-place | <small>[lambdalisue/fin.vim]</small>
| <kbd>\*</kbd> / <kbd>#</kbd> | 𝐍 𝐕 | Search selection forward/backward | <small>[haya14busa/vim-asterisk]</small>
| <kbd>g\*</kbd> / <kbd>g#</kbd> | 𝐍 𝐕 | Search whole-word forward/backward | <small>[haya14busa/vim-asterisk]</small>
| <kbd>Backspace</kbd> | 𝐍 | Match bracket | `%`
| <kbd>gp</kbd> | 𝐍 | Select last paste |
| <kbd>sg</kbd> | 𝐕 | Replace within selected area | `:s/⌴/gc`
| <kbd>Ctrl</kbd>+<kbd>r</kbd> | 𝐕 | Replace selection with step-by-step confirmation | `:%s/\V/⌴/gc`

### Clipboard

| Key   | Mode | Action             | Plugin or Mapping
| ----- |:----:| ------------------ | ------
| <kbd>p</kbd> | 𝐕 𝐒 | Paste without yank | <small>[kana/vim-operator-replace]</small>
| <kbd>Y</kbd> | 𝐍 | Yank to the end of line | `y$`
| <kbd>Space</kbd>+<kbd>y</kbd> | 𝐍 | Copy relative file-path to clipboard |
| <kbd>Space</kbd>+<kbd>Y</kbd> | 𝐍 | Copy absolute file-path to clipboard |

### Command & History

| Key   | Mode | Action             | Plugin or Mapping
| ----- |:----:| ------------------ | ------
| <kbd>!</kbd> | 𝐍 | Shortcut for shell command | `:!`
| <kbd>g!</kbd> | 𝐍 | Read vim command into buffer | `:put=execute('⌴')`
| <kbd>Ctrl</kbd>+<kbd>n</kbd> / <kbd>p</kbd> | 𝐂 | Switch history search pairs | <kbd>↓</kbd> / <kbd>↑</kbd>
| <kbd>↓</kbd> / <kbd>↑</kbd> | 𝐂 | Switch history search pairs | `Ctrl` `n`/`p`

### Editor UI

| Key   | Mode | Action             | Plugin or Mapping
| ----- |:----:| ------------------ | ------
| <kbd>Space</kbd>+<kbd>ts</kbd> | 𝐍 | Toggle spell-checker | <small>`:setlocal spell!`</small>
| <kbd>Space</kbd>+<kbd>tn</kbd> | 𝐍 | Toggle line numbers | <small>`:setlocal nonumber!`</small>
| <kbd>Space</kbd>+<kbd>tl</kbd> | 𝐍 | Toggle hidden characters | <small>`:setlocal nolist!`</small>
| <kbd>Space</kbd>+<kbd>th</kbd> | 𝐍 | Toggle highlighted search | <small>`:set hlsearch!`</small>
| <kbd>Space</kbd>+<kbd>tw</kbd> | 𝐍 | Toggle wrap | <small>`:setlocal wrap!`</small> …
| <kbd>Space</kbd>+<kbd>ti</kbd> | 𝐍 | Toggle indentation lines | <small>[nathanaelkane/vim-indent-guides]</small>
| <kbd>g1</kbd> | 𝐍 | Go to first tab | `:tabfirst`
| <kbd>g9</kbd> | 𝐍 | Go to last tab | `:tablast`
| <kbd>g5</kbd> | 𝐍 | Go to previous tab | `:tabprevious`
| <kbd>Ctrl</kbd>+<kbd>Tab</kbd> | 𝐍 | Go to next tab | `:tabnext`
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd><kbd>Tab</kbd> | 𝐍 | Go to previous tab | `:tabprevious`
| <kbd>Alt</kbd>+<kbd>j</kbd> | 𝐍 | Go to next tab | `:tabnext`
| <kbd>Alt</kbd>+<kbd>k</kbd> | 𝐍 | Go to previous tab | `:tabprevious`
| <kbd>Alt</kbd>+<kbd>{</kbd> | 𝐍 | Move tab backward | `:-tabmove`
| <kbd>Alt</kbd>+<kbd>}</kbd> | 𝐍 | Move tab forward | `:+tabmove`
| <kbd>Space</kbd>+<kbd>h</kbd> | 𝐍 | Show highlight groups for word |

### Custom Tools & Plugins

| Key   | Mode | Action             | Plugin or Mapping
| ----- |:----:| ------------------ | ------
| <kbd>-</kbd> | 𝐍 | Choose a window to edit | <small>[t9md/vim-choosewin]</small>
| <kbd>;</kbd>+<kbd>c</kbd> | 𝐍 | Open context-menu | <small>[plugin/actionmenu.vim]</small>
| <kbd>gK</kbd> | 𝐍 | Open Zeal or Dash on some file-types | <small>[plugin/devhelp.vim]</small>
| <kbd>g</kbd><kbd>Ctrl</kbd>+<kbd>o</kbd> | 𝐍 | Navigate to previous file on jumplist | <small>[plugin/jumpfile.vim]</small>
| <kbd>g</kbd><kbd>Ctrl</kbd>+<kbd>i</kbd> | 𝐍 | Navigate to next file on jumplist | <small>[plugin/jumpfile.vim]</small>
| <kbd>Space</kbd>+<kbd>l</kbd> | 𝐍 | Open side-menu helper | <small>[rafi/vim-sidemenu]</small>
| <kbd>Space</kbd>+<kbd>b</kbd> | 𝐍 | Open structure window | <small>[liuchengxu/vista.vim]</small>
| <kbd>Space</kbd>+<kbd>a</kbd> | 𝐍 | Show nearby tag in structure window | <small>[liuchengxu/vista.vim]</small>
| <kbd>Space</kbd>+<kbd>se</kbd> | 𝐍 | Save current workspace session | <small>[plugin/sessions.vim]</small>
| <kbd>Space</kbd>+<kbd>sl</kbd> | 𝐍 | Load workspace session | <small>[plugin/sessions.vim]</small>
| <kbd>Space</kbd>+<kbd>n</kbd>/<kbd>N</kbd> | 𝐍 | Open alternative file | <small>[kana/vim-altr]</small>
| <kbd>Space</kbd>+<kbd>tc</kbd> | 𝐍 | Enable scroll-context window | <small>[wellle/context.vim]</small>
| <kbd>Space</kbd>+<kbd>tp</kbd> | 𝐍 | Peek scroll-context window | <small>[wellle/context.vim]</small>
| <kbd>Space</kbd>+<kbd>S</kbd> | 𝐍 𝐕 | Source selection | `y:execute @@`
| <kbd>Space</kbd>+<kbd>?</kbd> | 𝐍 | Open the macOS dictionary on current word | `:!open dict://`
| <kbd>Space</kbd>+<kbd>P</kbd> | 𝐍 | Use Marked 2 for real-time Markdown preview | <small>[Marked 2]</small>
| <kbd>Space</kbd>+<kbd>ml</kbd> | 𝐍 | Append modeline to end of buffer | <small>[config/mappings.vim]</small>
| <kbd>Space</kbd>+<kbd>mda</kbd> | 𝐕 | Sequentially mark region for diff | <small>[AndrewRadev/linediff.vim]</small>
| <kbd>Space</kbd>+<kbd>mdf</kbd> | 𝐕 | Mark region for diff and compare if more than one | <small>[AndrewRadev/linediff.vim]</small>
| <kbd>Space</kbd>+<kbd>mds</kbd> | 𝐍 | Shows the comparison for all marked regions | <small>[AndrewRadev/linediff.vim]</small>
| <kbd>Space</kbd>+<kbd>mdr</kbd> | 𝐍 | Removes the signs denoting the diff regions | <small>[AndrewRadev/linediff.vim]</small>
| <kbd>Space</kbd>+<kbd>mg</kbd> | 𝐍 | Open Magit | <small>[jreybert/vimagit]</small>
| <kbd>Space</kbd>+<kbd>mt</kbd> | 𝐍 𝐕 | Toggle highlighted word | <small>[t9md/vim-quickhl]</small>
| <kbd>Space</kbd>+<kbd>-</kbd> | 𝐍 | Switch editing window with selected | <small>[t9md/vim-choosewin]</small>
| <kbd>Space</kbd>+<kbd>G</kbd> | 𝐍 | Toggle distraction-free writing | <small>[junegunn/goyo]</small>
| <kbd>Space</kbd>+<kbd>gu</kbd> | 𝐍 | Open undo-tree | <small>[mbbill/undotree]</small>
| <kbd>Space</kbd>+<kbd>K</kbd> | 𝐍 | Thesaurus | <small>[Ron89/thesaurus_query.vim]</small>
| <kbd>Space</kbd>+<kbd>W</kbd> | 𝐍 | VimWiki | <small>[vimwiki/vimwiki]</small>

### Window Management

| Key   | Mode | Action             | Plugin or Mapping
| ----- |:----:| ------------------ | ------
| <kbd>q</kbd> | 𝐍 | Quit window (and Vim, if last window) | `:quit`
| <kbd>Ctrl</kbd>+<kbd>q</kbd> | 𝐍 | Remap to C-w | <kbd>Ctrl</kbd>+<kbd>w</kbd>
| <kbd>Ctrl</kbd>+<kbd>x</kbd> | 𝐍 | Rotate window placement | `C-w` `x`
| <kbd>sv</kbd> | 𝐍 | Horizontal split | `:split`
| <kbd>sg</kbd> | 𝐍 | Vertical split | `:vsplit`
| <kbd>st</kbd> | 𝐍 | Open new tab | `:tabnew`
| <kbd>so</kbd> | 𝐍 | Close other windows | `:only`
| <kbd>sb</kbd> | 𝐍 | Previous buffer | `:b#`
| <kbd>sc</kbd> | 𝐍 | Close current buffer | `:close`
| <kbd>sx</kbd> | 𝐍 | Delete buffer, leave blank window | `:enew │ bdelete`
| <kbd>sz</kbd> | 𝐍 | Toggle window zoom | `:vertical resize │ resize`
| <kbd>ssv</kbd> | 𝐍 | Split with previous buffer | `:split │ wincmd p │ e#`
| <kbd>ssg</kbd> | 𝐍 | Vertical split with previous buffer | `:vsplit │ wincmd p │ e#`
| <kbd>sh</kbd> | 𝐍 | Toggle colorscheme background=dark/light | `:set background` …
| <kbd>s-</kbd> | 𝐍 | Lower solarized8 colorscheme contrast | `:colorscheme ` …
| <kbd>s=</kbd> | 𝐍 | Raise solarized8 colorscheme contrast | `:colorscheme ` …

### Git Version Control

| Key   | Mode | Action             | Plugin or Mapping
| ----- |:----:| ------------------ | ------
| <kbd>gs</kbd> | 𝐍 | Preview hunk | <small>[airblade/vim-gitgutter]</small>
| <kbd>gS</kbd> | 𝐍 𝐕 𝐒 | Stage hunk | <small>[airblade/vim-gitgutter]</small>
| <kbd>Space</kbd>+<kbd>gr</kbd> | 𝐍 | Revert hunk | <small>[airblade/vim-gitgutter]</small>
| <kbd>Space</kbd>+<kbd>ga</kbd> | 𝐍 | Git add current file | <small>[lambdalisue/gina.vim]</small>
| <kbd>Space</kbd>+<kbd>gd</kbd> | 𝐍 | Git diff | <small>[lambdalisue/gina.vim]</small>
| <kbd>Space</kbd>+<kbd>gc</kbd> | 𝐍 | Git branches | <small>[lambdalisue/gina.vim]</small>
| <kbd>Space</kbd>+<kbd>gc</kbd> | 𝐍 | Git commit | <small>[lambdalisue/gina.vim]</small>
| <kbd>Space</kbd>+<kbd>gb</kbd> | 𝐍 | Git blame | <small>[lambdalisue/gina.vim]</small>
| <kbd>Space</kbd>+<kbd>gs</kbd> | 𝐍 | Git status -s | <small>[lambdalisue/gina.vim]</small>
| <kbd>Space</kbd>+<kbd>gl</kbd> | 𝐍 | Git log --all | <small>[lambdalisue/gina.vim]</small>
| <kbd>Space</kbd>+<kbd>gF</kbd> | 𝐍 | Git fetch | <small>[lambdalisue/gina.vim]</small>
| <kbd>Space</kbd>+<kbd>gp</kbd> | 𝐍 | Git push | <small>[lambdalisue/gina.vim]</small>
| <kbd>Space</kbd>+<kbd>go</kbd> | 𝐍 𝐕 | Open SCM detailed URL in browser | <small>[lambdalisue/gina.vim]</small>

### Plugin: Denite

| Key   | Mode | Action
| ----- |:----:| ------------------
| <kbd>;r</kbd> | 𝐍 | Resumes last Denite window
| <kbd>;f</kbd> | 𝐍 | File search
| <kbd>;g</kbd> | 𝐍 | Grep search
| <kbd>;b</kbd> | 𝐍 | Buffers
| <kbd>;i</kbd> | 𝐍 | Old files
| <kbd>;x</kbd> | 𝐍 | Most recently used files (MRU)
| <kbd>;d</kbd> | 𝐍 | Directories and MRU
| <kbd>;v</kbd> | 𝐍 𝐕 | Yank history
| <kbd>;l</kbd> | 𝐍 | Location list
| <kbd>;q</kbd> | 𝐍 | Quick fix
| <kbd>;m</kbd> | 𝐍 | Marks
| <kbd>;n</kbd> | 𝐍 | Dein plugin list
| <kbd>;j</kbd> | 𝐍 | Jump points and change stack
| <kbd>;u</kbd> | 𝐍 | Junk files
| <kbd>;o</kbd> | 𝐍 | Outline tags
| <kbd>;s</kbd> | 𝐍 | Sessions
| <kbd>;t</kbd> | 𝐍 | Tag list
| <kbd>;p</kbd> | 𝐍 | Jumps
| <kbd>;h</kbd> | 𝐍 | Help
| <kbd>;w</kbd> | 𝐍 | Memo list
| <kbd>;z</kbd> | 𝐍 | Z (jump around)
| <kbd>;;</kbd> | 𝐍 | Command history
| <kbd>;/</kbd> | 𝐍 | Buffer lines
| <kbd>;\*</kbd> | 𝐍 | Search word under cursor with lines
| <kbd>Space</kbd>+<kbd>gt</kbd> | 𝐍 | Find tags matching word under cursor
| <kbd>Space</kbd>+<kbd>gf</kbd> | 𝐍 | Find files matching word under cursor
| <kbd>Space</kbd>+<kbd>gg</kbd> | 𝐍 𝐕 | Grep word under cursor
| **Within _Denite_ window** ||
| <kbd>jj</kbd> or <kbd>Escape</kbd> | 𝐈 | Leave Insert mode
| <kbd>i</kbd> or <kbd>/</kbd> | 𝐍 | Enter Insert mode (filter input)
| <kbd>q</kbd> or <kbd>Escape</kbd> | 𝐍 | Exit denite window
| <kbd>Tab</kbd> or <kbd>Shift</kbd>+<kbd>Tab</kbd> | 𝐈 | Next/previous candidate
| <kbd>Space</kbd> | 𝐍 | Select candidate entry
| <kbd>dd</kbd> | 𝐍 | Delete entry
| <kbd>p</kbd> | 𝐍 | Preview entry
| <kbd>st</kbd> | 𝐍 | Open in a new tab
| <kbd>sg</kbd> | 𝐍 | Open in a vertical split
| <kbd>sv</kbd> | 𝐍 | Open in a split
| <kbd>'</kbd> | 𝐍 | Quick-move
| <kbd>r</kbd> | 𝐍 | Redraw
| <kbd>yy</kbd> | 𝐍 | Yank
| <kbd>Tab</kbd> | 𝐍 | List and choose action

### Plugin: Defx

| Key   | Mode | Action
| ----- |:----:| ------------------
| <kbd>;e</kbd> | 𝐍 | Open file-explorer (toggle)
| <kbd>;a</kbd> | 𝐍 | Focus current file in file-explorer
| **Within _Defx_ window** ||
| <kbd>j</kbd> or <kbd>k</kbd> | 𝐍 | Move up and down the tree
| <kbd>l</kbd> or <kbd>Return</kbd> | 𝐍 | Toggle collapse/expand directory or open file
| <kbd>h</kbd> | 𝐍 | Collapse directory tree
| <kbd>t</kbd> | 𝐍 | Expand directory tree recursively
| <kbd>.</kbd> | 𝐍 | Toggle hidden files
| <kbd>Space</kbd> | 𝐍 | Select entry
| <kbd>\*</kbd> | 𝐍 | Invert selection (select all)
| <kbd>&</kbd> or <kbd>\</kbd> | 𝐍 | Change into current working directory
| <kbd>~</kbd> | 𝐍 | Change to user home directory
| <kbd>u</kbd> or <kbd>Backspace</kbd> | 𝐍 | Change into parent directory
| <kbd>u</kbd> <kbd>2</kbd>/<kbd>3</kbd>/<kbd>4</kbd> | 𝐍 | Change into parent directory count
| <kbd>st</kbd> | 𝐍 | Open file in new tab
| <kbd>sv</kbd> | 𝐍 | Open file in a horizontal split
| <kbd>sg</kbd> | 𝐍 | Open file in a vertical split
| <kbd>N</kbd> | 𝐍 | Create new directories and/or files
| <kbd>K</kbd> | 𝐍 | Create new directory
| <kbd>c</kbd> / <kbd>m</kbd> / <kbd>p</kbd> | 𝐍 | Copy, move, and paste
| <kbd>r</kbd> | 𝐍 | Rename file or directory
| <kbd>dd</kbd> | 𝐍 | Trash selected files and directories
| <kbd>y</kbd> | 𝐍 | Yank path to clipboard
| <kbd>w</kbd> | 𝐍 | Toggle window size
| <kbd>]g</kbd> | 𝐍 | Next dirty git item
| <kbd>[g</kbd> | 𝐍 | Previous dirty git item
| <kbd>x</kbd> or <kbd>gx</kbd> | 𝐍 | Execute associated system application
| <kbd>gd</kbd> | 𝐍 | Open git diff on selected file
| <kbd>gl</kbd> | 𝐍 | Open terminal file explorer with tmux
| <kbd>gr</kbd> | 𝐍 | Grep in current position
| <kbd>gf</kbd> | 𝐍 | Find files in current position

### Plugin: Clap

| Key   | Mode | Action
| ----- |:----:| ------------------
| **Within _Clap_ window** ||
| <kbd>jj</kbd> or <kbd>Escape</kbd> | 𝐈 | Leave Insert mode
| <kbd>i</kbd> | 𝐍 | Enter Insert mode (filter input)
| <kbd>q</kbd> or <kbd>Escape</kbd> | 𝐍 | Exit clap window
| <kbd>Tab</kbd> or <kbd>Shift</kbd>+<kbd>Tab</kbd> | 𝐈 | Next/previous candidate
| <kbd>Space</kbd> or <kbd>\'</kbd> | 𝐍 | Select candidate entry
| <kbd>st</kbd> | 𝐍 | Open in a new tab
| <kbd>sg</kbd> | 𝐍 | Open in a vertical split
| <kbd>sv</kbd> | 𝐍 | Open in a split

### Plugin: Asyncomplete and Emmet

| Key   | Mode | Action
| ----- |:----:| ------------------
| <kbd>Tab</kbd> / <kbd>Shift-Tab</kbd> | 𝐈 | Navigate completion-menu
| <kbd>Enter</kbd> | 𝐈 | Select completion or expand snippet
| <kbd>Ctrl</kbd>+<kbd>j</kbd>/<kbd>k</kbd>/<kbd>d</kbd>/<kbd>u</kbd> | 𝐈 | Movement in completion pop-up
| <kbd>Ctrl</kbd>+<kbd>Return</kbd> | 𝐈 | Expand Emmet sequence
| <kbd>Ctrl</kbd>+<kbd>Space</kbd> | 𝐈 | Refresh and show candidates
| <kbd>Ctrl</kbd>+<kbd>y</kbd> | 𝐈 | Close pop-up
| <kbd>Ctrl</kbd>+<kbd>e</kbd> | 𝐈 | Cancel selection and close pop-up
| <kbd>Ctrl</kbd>+<kbd>l</kbd> | 𝐈 | Expand snippet at cursor
| <kbd>Tab</kbd> / <kbd>Shift-Tab</kbd> | 𝐈 𝐒 | Navigate snippet placeholders

### Plugin: Any-Jump

| Key   | Mode | Action
| ----- |:----:| ------------------
| <kbd>Space</kbd>+<kbd>ii</kbd> | 𝐍 | Jump to definition under cursor
| <kbd>Space</kbd>+<kbd>ii</kbd> | 𝐕 | Jump to selected text in visual mode
| <kbd>Space</kbd>+<kbd>ib</kbd> | 𝐍 | Open previous opened file (after jump)
| <kbd>Space</kbd>+<kbd>il</kbd> | 𝐍 | Open last closed search window again

### Plugin: Signature

| Key   | Mode | Action
| ----- |:----:| ------------------
| <kbd>m/</kbd> or <kbd>m?</kbd> | 𝐍 | Show list of buffer marks/markers
| <kbd>mm</kbd> | 𝐍 | Toggle mark on current line
| <kbd>m,</kbd> | 𝐍 | Place next mark
| <kbd>m</kbd> <kbd>a-z</kbd> | 𝐍 | Place specific mark (Won't work for: <kbd>mm</kbd>, <kbd>mn</kbd>, <kbd>mp</kbd>)
| <kbd>dm</kbd> <kbd>a-z</kbd> | 𝐍 | Remove specific mark (Won't work for: <kbd>mm</kbd>, <kbd>mn</kbd>, <kbd>mp</kbd>)
| <kbd>mn</kbd> | 𝐍 | Jump to next mark
| <kbd>mp</kbd> | 𝐍 | Jump to previous mark
| <kbd>]=</kbd> | 𝐍 | Jump to next marker
| <kbd>[=</kbd> | 𝐍 | Jump to previous marker
| <kbd>m-</kbd> | 𝐍 | Purge all on current line
| <kbd>m</kbd> <kbd>Space</kbd> | 𝐍 | Purge marks
| <kbd>m</kbd> <kbd>Backspace</kbd> | 𝐍 | Purge markers

</details>

## Credits & Contribution

Big thanks to the dark knight [Shougo](https://github.com/Shougo).

[config/mappings.vim]: ./config/mappings.vim
[plugin/whitespace.vim]: ./plugin/whitespace.vim
[plugin/sessions.vim]: ./plugin/sessions.vim
[plugin/devhelp.vim]: ./plugin/devhelp.vim
[plugin/jumpfile.vim]: ./plugin/jumpfile.vim
[plugin/actionmenu.vim]: ./plugin/actionmenu.vim
[config/plugins/lsp.vim]: ./config/plugins/lsp.vim
[Marked 2]: https://marked2app.com
[Neovim]: https://github.com/neovim/neovim
[Vim]: https://github.com/vim/vim
[lazy-loaded]: ./config/plugins.yaml#L47
