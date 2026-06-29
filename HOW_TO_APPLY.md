# Apply update: navy theme, FABLE logo, People page, publications setup

Only the files that changed/are new are here. You do NOT re-push the whole site.

## Steps
1. Open your cloned `mowgli89.github.io` folder.
2. Copy the CONTENTS of this folder into it, keeping the same paths; overwrite when asked.
3. GitHub Desktop will show the changed/new files (about 16), not the whole site.
4. Summary: "Theme, logo, people page, publications". Commit to main, then Push origin.
   The live site rebuilds in a few minutes.

## What changed
- _config.yml ............... lab name + description
- _pages/about.md .......... navy tagline; homepage image = FABLE mark
- _pages/people.md ......... NEW: PI bio (headshot placeholder) + lab members
- _pages/publications.md ... nav order only
- _pages/contact.md ........ nav order only
- _sass/_themes.scss ....... NEW: navy theme color
- _data/members.yml ........ NEW: edit THIS to add/remove lab members (see notes in file)
- _bibliography/papers.bib . publications; import your ORCID BibTeX here (instructions inside)
- assets/img/fable_* ....... logo files (mark + lockup, svg + png) + favicon
- assets/img/headshot_placeholder.png ... PI photo placeholder (replace with real headshot)
- assets/img/members/member_placeholder.png ... default member photo

## Two quick to-dos for you
1. PUBLICATIONS: open _bibliography/papers.bib and paste your ORCID BibTeX export
   (orcid.org > Works > Export > BibTeX). Renders automatically on /publications/.
2. PEOPLE: replace assets/img/headshot_placeholder.png with your real headshot,
   and edit _data/members.yml to list your actual team. Photos go in assets/img/members/.
