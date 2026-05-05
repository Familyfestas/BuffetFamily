# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository scope

This repository currently contains a single asset: `buffetfamilysite.txt` — a self-contained HTML landing page (in Portuguese, `lang="pt-BR"`) for **Buffet Family Festas Kids**, a children's party venue with locations in Capão Redondo, Kizaemon, Butantã, and Taboão da Serra (São Paulo, Brazil).

There is no build system, package manager, test suite, or linter. Treat the repo as a single static document, not an application.

## Working with `buffetfamilysite.txt`

- Despite the `.txt` extension, the file is a complete HTML5 document (`<!DOCTYPE html>` … `</html>`) with inline CSS in a `<style>` block and no external JS or assets. Edits should preserve that single-file, no-dependencies shape — do not split CSS into separate files or introduce build steps unless the user explicitly asks.
- To preview, open the file directly in a browser, or rename/copy to `.html` locally. Do not rename the tracked file without the user's say-so.
- All copy is Portuguese (pt-BR). Keep new copy in pt-BR unless the user asks otherwise, and preserve emoji used in headings (🎉, 📸, 📲, 💬) — they are part of the visual design, not decoration to strip.
- The page hardcodes business-critical links and details that should not be changed casually:
  - Calendly: `https://calendly.com/buffetfamily`
  - WhatsApp: `https://wa.me/5511940720384`
  - Promotion copy ("+10 convidados grátis", "Apenas 2 vouchers") and the unit list
- Color palette in use: `#ff69b4` (header pink), `#25d366` (WhatsApp green CTA), `#fff7f0` (page background). Reuse these rather than introducing new brand colors.

## Git workflow

- Default branch is `main`. Active development for this task happens on `claude/add-claude-documentation-0WuR4` per the harness instructions; follow whatever branch the current task specifies and push with `git push -u origin <branch>`.
- Do not open pull requests unless the user explicitly asks.
