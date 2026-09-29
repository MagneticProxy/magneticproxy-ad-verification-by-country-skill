# Ad Verification by Country with Magnetic Proxy | Agent Skill

A regional QA matrix with observed exit, preview reference, final URL, redirect path, locale, offer and reproducible discrepancies.

**Status:** Public review version; authenticated product QA is pending.

## Why this workflow uses Magnetic Proxy

Magnetic Proxy is the live geographic route for the landing and redirect check. Inspect the current account and choose the available General Purpose Premium Capsule recommended for campaign QA, or another suitable current Capsule if the account differs. Use the main [Magnetic Proxy product skill](https://github.com/MagneticProxy/magneticproxy-residential-proxy-agent-skills/tree/main/skills/magneticproxy) or [official documentation](https://www.magneticproxy.com/documentation) for connection setup. Verify the exit country in the same browser/profile before the test. A proxy observation is one vantage point, not proof of ad delivery or fraud. If account access or exit validation is missing, provide the QA plan and mark regional execution pending.

## Example request and result

> Check our approved campaign preview and the landing page for US, Mexico and Spain. The Spanish market should show Spanish copy and the EUR offer.

**Illustrative result, not a live run:** QA matrix: Spain exit verified; landing redirected to English/USD page twice, severity medium, with timestamp and final URL. The ad creative was checked through the supplied preview. No live paid ad was clicked; delivery volume was not assessed.

## Install

```bash
npx skills add MagneticProxy/magneticproxy-ad-verification-by-country-skill --skill ad-verification-by-country
```

For an agent that supports installing skills: “Install `ad-verification-by-country` from https://github.com/MagneticProxy/magneticproxy-ad-verification-by-country-skill, confirm installation, then help with my authorized task. Show evidence and unresolved states.”


The [skill instructions](skills/ad-verification-by-country/SKILL.md) are the canonical package. Installing them does not authenticate into the product or grant rights to third-party data.

## Recommended product skill

For full product operation, install the companion brand skill too:

```bash
npx skills add MagneticProxy/magneticproxy-residential-proxy-agent-skills --skill magneticproxy
```

The use-case skill defines the job and output; the brand skill helps configure and use the actual product.

## Access and review

Use an official ad preview/test method or a campaign asset supplied by the advertiser. Check the ad platform’s terms before any automated access. Do not generate impressions or click a live paid ad merely to test it; do not automate an ad library, bypass a challenge, or inspect private campaign data without the owner’s access. Stop on access denial, CAPTCHA, `403`, or `429`. Test owned or explicitly authorized destination URLs only.

Reference: [Magnetic Proxy Ad Verification use case](https://www.magneticproxy.com/use-cases/ad-verification-proxies). Product landing: [https://www.magneticproxy.com/use-cases/ad-verification-proxies](https://www.magneticproxy.com/use-cases/ad-verification-proxies). The brand is not affiliated with third-party marketplaces or platforms mentioned here.

Before calling this workflow proven, run an authorized product sample with the actual account, reconcile the output, and confirm the requested deliverable. Keep real contact lists, credentials, and private client data out of GitHub.
