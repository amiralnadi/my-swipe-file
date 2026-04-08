# my-swipe-file
  Your personal swipe file — a curated library of references, examples, and inspiration, connected to [myswipe.cc](https://myswipe.cc).
                                                                                                                                                        
  ## What is a swipe file?
                                                                                                                                                        
  A swipe file is a collection of things you find valuable and want to reference later: great copy, design examples, useful frameworks, interesting
  articles. Instead of forgetting them in browser bookmarks, you build a searchable library you actually use in your work.                              
                                                                                                                          
  ## Getting started                                                                                                                                    
                                                            
  1. Fork this repo (click **Fork** in the top right)
  2. Go to [myswipe.cc](https://myswipe.cc) and sign in with GitHub
  3. Grant the app access to your forked repo                      
  4. Your swipe file is ready

## Why Markdown + GitHub?
                                                                                                                                                        
  Your items are plain Markdown files in your own GitHub repo. This means AI tools like Claude, Cursor, or Copilot can read them natively.
                                                                                                                                                        
  Point your AI at this repo and it has access to your entire reference library. When you're writing copy, designing a feature, or solving a problem, your AI can draw from your specific examples and standards instead of giving you generic output. The more you save, the more personalized and useful your AI becomes.                                                                                                                                      
                                                            
  This is your **personal knowledge base** — built in a format AI understands natively.        
                             
  ## Adding items                                                                                                                                       
                                                            
  **Via the web app** — click the + button at myswipe.cc                                                                                                
                                                            
  **Via Claude Code** — install the `/myswipe` skill, then run:
  /myswipe add https://example.com                                                                                                                      
  Claude will fetch the page and fill in the card automatically — title, category, tags, description, when to use it.
                                                                                                                                                        
  **Manually** — edit the Markdown files in `data/` directly in any editor
                                                                                                                                                        
  ## Using with Claude Code (/myswipe skill)

  Most people save links they never return to. Bookmarks pile up, tabs stay open, notes get lost. The /myswipe skill fixes this by turning anything you find interesting into a structured, searchable item in your
  library — and making that library actually useful when you work.

  ### What you can do

  **Keep all your bookmarks valuable:**
  - `/myswipe add [url] + [note] (optionally)` — Claude fills in the card automatically, and then you can extract value when you actually need it. Your saved guides, references, tools and other 
  - `/myswipe add https://twitter.com/... great example of a launch thread that went viral` — add a note alongside the link, AI uses it as context to write a better card
  - `/myswipe add https://somesite.com — just drop a link, no note needed`

  **Surface relevant references while you work:**
  - `/myswipe check` — tell Claude what you're working on, it scans your library and shows you the most relevant items with an explanation of why each one applies

  **Example use cases:**
  - Writing a cold email sequence → `/myswipe check` surfaces the email examples and copywriting frameworks you've saved
  - Designing a landing page → it finds the SaaS landing pages and conversion examples from your library
  - Planning a social media campaign → it pulls your saved UGC platforms, viral threads, and campaign references

  The more you save, the more useful it gets. Your library becomes a personalized knowledge base that makes your AI outputs less generic, more aligned with your expectations and more grounded in examples you've already vetted.

  ### Install the skill

  Paste this single command in your terminal — it creates the skill folder and downloads the skill file in one step:

  ```bash
  mkdir -p ~/.claude/skills/myswipe && curl -s https://raw.githubusercontent.com/amiralnadi/swipe-file/main/skill.md -o ~/.claude/skills/myswipe/skill.md

  Then complete the one-time setup:
  1. Go to myswipe.cc/settings and copy your API key
  2. Run /myswipe setup in Claude Code and paste the key when prompted
  3. Done — the skill works in both Claude Code CLI and desktop app
  
  
  ## Data format
                                                                                                                                                        
  Each `.md` file in `data/` is a folder. Items follow this structure:
                                                                                                                                                        
  ```markdown
  ---                                                                                                                                                   
  folder: Design                                            
  description: Design references and inspiration
  ---                                           
     
  ## Category Name
                                                                                                                                                        
  ### Item Title
  - Link: https://example.com                                                                                                                           
  - Image: https://example.com/image.jpg                    
  - Tags: tag1, tag2, tag3              
  - Description: Why this is worth saving                                                                                                               
  - When to use: The situation where this is relevant
  - Added: 2024-01-01                                                                                                                                   
                                                                                                                                                        
  Structure
                                                                                                                                                        
  data/                                                     
  ├── design.md        # Design references
  ├── marketing.md     # Marketing and growth                                                                                                           
  └── copywriting.md   # Copy examples
