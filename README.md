# OWASP FinBot CTF Workshop Walkthrough

Working payloads and walkthroughs for the 5 challenges run during the OWASP Capture the Flag workshop at **Cloud Tech Show Frankfurt, 6 May 2026, 15:45–17:30, The Collaboration Hub**.

**Live walkthrough:** [dansecops.github.io/finbot-frankfurt](https://dansecops.github.io/finbot-frankfurt/)

**Platform:** [owasp-finbot-ctf.org](https://owasp-finbot-ctf.org/)

## What's in here

The walkthrough covers the 5 demoed challenges plus a "try at home" path for the other 14 challenges on the platform.

1. `recon-onboarding` — Beginner. Leak the agent's vendor evaluation rules. Two badges.
2. `policy-bypass-invoice-threshold` — Intermediate. Approve a $75k invoice over the platform's hard cap.
3. `data-exfil-double-agent` — Intermediate. Poison a tool, watch the platform exfiltrate vendor data.
4. `rce-shell-shock` — Intermediate. Multi-turn foot-in-the-door RCE.
5. `labs-guardrail-101` — Beginner defensive. Block any tool call with a webhook.

## Contact

- **OWASP Frankfurt Chapter** — search "OWASP Frankfurt" on LinkedIn

## Building the site

`public-cheatsheet.md` is the source. `index.html` is rendered from it by `.github/workflows/pages.yml` on every push to `main` and deployed to GitHub Pages — it is not committed.

Preview locally:

```bash
pandoc public-cheatsheet.md -o index.html --standalone \
  --include-before-body=header.html --css=style.css \
  --metadata title="OWASP FinBot CTF: Workshop Walkthrough"
python3 -m http.server 8080
# open http://localhost:8080/
```

## License

Content released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Use it, remix it, attribute back.
