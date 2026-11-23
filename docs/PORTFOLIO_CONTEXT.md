# Portfolio context (read this first)

Owner: Abdelrahman Ezzat (company QN VENTURES LTD, UK no. 17391834, partner Zohdy 30%). Status date: 2026-11-23.
This file explains where this repository fits in the whole portfolio. It is the same story in every repository, followed by a section specific to this one.

## Target layout (agreed 2026-11-23, being migrated step by step, nothing deleted)
- Group 1, QuNeva: GitHub org `quneva`, Supabase project `QuNeva` (currently `QuNeva_M`), domain quneva.com. Flagship and most critical.
- Group 2, QN Ventures products: GitHub org `qn-ventures`, Supabase project `QN-Products` (currently `QN-AI.Portfolio`, ref kefoipujbrnfujqxidbv; one schema per product). Store and customer apps live together in the repo `qn-apps` (Noor, Sahra, Sofra, BabyBoard public edition, Finance public edition, QN-AI, InsightGrid and WFM Flow store editions). `Dashboard`, `qn-website`, `qn-company`, `qn-brain` are separate repos.
- Group 3, owner personal (the partner has no access): the owner's personal GitHub account and a separate Supabase org `Personal` with project `QN-Personal`. Holds Portfolio, ops console, Furja, Home Assistant add-on, the owner's own BabyBoard and Finance data, and the personal `brain` repo.

## Rules that apply everywhere
1. Production must never go down. Every migration step copies first, verifies, then switches, with a written rollback. Nothing is deleted from the source.
2. Deploy by git push (Cloudflare Workers Builds / Pages). Never ask for or use a Cloudflare token that can edit Workers: such a token reaches every Worker in the account, including personal ones.
3. Try changes on a preview before production, especially QuNeva and Dashboard.
4. Secrets live only in the provider dashboards. Their names (never values) are listed in the private `qn-brain` repo.
5. Write everything stored in repositories (docs, commits, PRs) in plain English.
6. Google Play: only these apps may be published: QuNeva (com.quneva.wfm), InsightGrid store edition (uk.qnventures.insights), WFM Flow store edition (uk.qnventures.flow), Finance (uk.qnventures.finance), Noor (uk.qnventures.noor), BabyBoard (appeal pending). The full Dashboard platform must NEVER be published on Google Play (the unpublished package uk.qnventures.insightgrid is bound to da.abdelrahman-ezzat.com and must stay unpublished).
7. Claude conversations are named per project (see "Conversation" below) and each starts by reading the private `qn-brain` repository: `share/QN_Ventures_Map_for_Partner_EN.html` (partner-safe map), `projects/FINAL_MAP.html` (full map, owner only) and `projects/DECISIONS_2026-11-23.md`.

## This repository
- Role: Home Assistant add-on (Music Assistant Alexa API).
- Target home: Group 3 (personal).
- Domains: ha.abdelrahman-ezzat.com (Cloudflare tunnel)
- Database: none
- Claude conversation name: Home Assistant

This file only describes context. It changes no behavior.
