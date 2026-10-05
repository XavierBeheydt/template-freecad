# AI Instructions

This file provides guidance to AI coding agents (Claude Code, and other
agents reading it via the `AGENTS.md` symlink) when working in this
repository.

## Project overview

This is a personal FreeCAD modeling project, not a software project — there
is no build, lint, or test tooling. The goal is to design a 3D-printable
<!-- TODO: one sentence on what the part is and what it does -->, as
described in [README.md](README.md).

## Repository structure

- `cad/` — FreeCAD source file (`.FCStd`).
- `exports/` — 3MF exports for slicing and printing (full assembly, and
  each part separately when there are several).
- `images/` — renders, slicer screenshots and print photos (PNG).

## Language

Write everything in this repository — README, commit messages, code
comments, docs — in English only. Conversation with the user can be in
whichever language they use.

## Working with the FreeCAD file

- `.FCBak` backup files and the `backup/` directory are gitignored — never
  commit them.
- The `.FCStd` file is a binary FreeCAD document; it can't be reviewed as a
  text diff, so describe what changed in the commit message instead.

## Images

- Store photos as PNG in `images/`, with descriptive kebab-case names
  (`print-desk-filled.png`, not `IMG_1234.png`).
- When converting phone photos, apply the EXIF rotation and strip metadata
  (GPS included): `magick in.jpeg -auto-orient -strip out.png`.

## Printables listing

The Printables.com description is drafted in `PRINTABLES.md` at the repo
root. It is a temporary file and is gitignored — never commit it.

If the model is a remake or remix of someone else's design, credit the
original (link, title, author) in the README and in the listing, and check
its license: a ShareAlike license means this repository must use the same
one.
