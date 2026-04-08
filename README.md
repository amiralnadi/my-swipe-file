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
