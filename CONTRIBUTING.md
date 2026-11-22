# Contributing to Auditory Atlas

Contributions, corrections, and suggestions of auditory neuroscience or computational audiology laboratories are welcome via **GitHub Issues** or **Pull Requests**.

## Verification Requirements for Laboratory Submissions

To prevent link hijacking, spam, and unverified entries, every submission or URL change must satisfy:

1. **Official Institutional `https://` URLs:** Both the lab site (`lab_url`) and careers/opportunities page (`careers_url`) must point directly to an official university, research institute, or verified lab domain using `https://` whenever supported. URL shorteners, affiliate trackers, or third-party redirects are rejected.
2. **Primary Bibliographic Verification:** Include the Principal Investigator's **OpenAlex Author ID** (`A...`) and/or **ORCID** (`0000-0000-0000-0000`) plus institutional city/country.
3. **Accurate Classification:** Research pillars (`abr_eeg`, `mri_neuroanatomy`, `cochlear_efferent`, `aging_tinnitus`, `ci_psychoacoustics`, `comp_audiology`) and thematic tags must reflect published, peer-reviewed work. Metrics and `fit_score` are generated strictly from OpenAlex/Europe PMC metadata and are never manually inflated.
4. **Data Privacy:** Do **not** submit private personal emails, phone numbers, or non-public contact information.
5. **Security & CSP Maintenance:** `index.html` enforces a hash-pinned `<meta http-equiv="Content-Security-Policy">` with no `'unsafe-inline'`. Any Pull Request touching `<script>` or `<style>` inside `index.html` must recompute the SHA-256 hashes in `<head>` and verify zero CSP console violations in Chromium.
