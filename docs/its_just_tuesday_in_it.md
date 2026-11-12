# It's Just Tuesday in IT: Why Sysadmins Sound Like Spies

**Authors:** Danielle C. & Vesper Luna | CC-0

---

If you've read anything in the Gesamtkunstwerk library and found yourself thinking "this person sounds like an intelligence analyst" — you're not wrong. The vocabulary overlaps significantly. What you may not know is that this vocabulary is entirely standard in IT systems engineering. It's not tradecraft. It's the job.

This document is a brief translation guide.

---

## RCA — Root Cause Analysis

**What it sounds like:** Intelligence debrief methodology. Systematic causal chain reconstruction. Post-incident forensic analysis.

**What it actually is:** Standard procedure after any significant system outage. When a server goes down, you don't just restart it and move on. You trace back through logs, configurations, change histories, and system dependencies to find what actually caused the failure — so it doesn't happen again.

IT escaped a trap that catches many other diagnostic fields: **downtime only costs money. There is no scenario where a sysadmin profits from the server staying down.**

In fields where payment structures reward ongoing treatment over durable resolution — mechanics paid per repair, advisors paid on commission, any context where recurring revenue beats a permanent fix — the incentive quietly tilts away from root cause and toward symptom management. This isn't usually individual malice. It's the predictable behavior of rational actors responding to the incentives they're given.

The Ford Pinto is the clearest example: Ford's engineers ran a cost-benefit analysis and determined that paying wrongful death settlements was cheaper than recalling the defective fuel tank. Even the legal liability incentive — which should produce rigorous RCA — can be overridden by a sufficiently cynical spreadsheet.

IT doesn't have that escape hatch. When Amazon.com goes down, the cost is estimated at roughly $220,000 per minute. Whether you're an internal sysadmin at a major retailer or a managed services engineer, the incentive is total and unambiguous: find the actual cause, fix it permanently, prevent recurrence. The server is either up or it isn't. The accountability is immediate and visible. The profit motive accidentally produced good epistemology in IT because the math only points one direction.

RCA is just what you do when failure is visible and downtime is expensive.

---

## OSINT — Open Source Intelligence

**What it sounds like:** Covert information gathering methodology. Intelligence tradecraft.

**What it actually is:** Googling with structure and intention.

Every IT professional who has ever debugged a weird error by searching forums, checked a vendor's public documentation, cross-referenced a CVE database, or verified a configuration against publicly available specs is doing OSINT. We just call it "looking it up" or "doing research."

OSINT specifically means gathering information from publicly available sources — no classified access, no covert methods, no NDAs required. It's the opposite of classified intelligence work. Everything in the Gesamtkunstwerk library was built from public sources: FOIA data, peer-reviewed papers, declassified documents, publicly available satellite gravimetry, forum posts, and Wikipedia rabbit holes. That's OSINT. That's also just research.

The difference between an OSINT analyst and someone Googling is methodology: systematic sourcing, cross-referencing, verification, and documentation of the chain of evidence. Which is also just good research practice. Which is also just IT documentation standards applied to information rather than infrastructure.

---

## HUMINT — Human Intelligence

**What it sounds like:** Running informants. Covert human source networks.

**What it actually is:** Social engineering awareness training. We get it annually.

Every IT department with a security budget runs training on how threat actors extract information through human interaction: pretexting (calling the helpdesk claiming to be an executive who locked themselves out), phishing (email that looks legitimate), vishing (voice phishing), tailgating (following someone through a secure door). We learn these attack vectors so we can defend against them.

That's HUMINT from the defensive posture. Understanding how human intelligence gathering works is a prerequisite for not being a victim of it. IT professionals who've sat through this training a few times start to notice the same patterns in other contexts — not because they're spooks, but because pattern recognition trained for one domain transfers.

---

## Threat Modeling

**What it sounds like:** Intelligence assessment. Adversarial analysis.

**What it actually is:** Standard security engineering practice.

Before deploying any significant system, security-conscious IT teams ask: Who are the potential adversaries? What do they want? What are the attack surfaces? What's the likely attack path? What's the impact if they succeed?

This is called threat modeling. It's in the OWASP documentation. It's taught in security certifications. It's what you do before you put anything on the internet that matters.

Applying threat modeling to non-technical situations — political, personal, institutional — is just the same analytical framework operating on a different subject. The methodology transfers because adversaries operate similarly regardless of domain.

---

## Compartmentalization / Need-to-Know

**What it sounds like:** Classified information handling. Covert operational security.

**What it actually is:** Role-based access control. Standard managed services practice.

In any managed services environment handling multiple clients, technicians don't have access to every client's systems. Client A's configuration, credentials, and data are not visible to technicians working on Client B's account. This isn't secrecy theater — it's liability management, data privacy compliance, and basic professional ethics.

The principle is identical to classified information handling: people access what they need to do their jobs and nothing more. The difference is that IT does it to protect clients from each other, not to protect state secrets.

---

## CC-0 — Public Domain Dedication

**What it sounds like:** Radical information liberation philosophy.

**What it actually is:** Open-source ethos. Same reason your sysadmin uses Linux.

The open-source software movement was built on the premise that software should be freely available, modifiable, and shareable. Linux — the operating system running most of the world's servers, smartphones, and supercomputers — was built collaboratively by people who shared their work freely. Stack Overflow exists because developers share solutions without expecting payment. GitHub repositories are public by default because sharing is how the field advances.

CC-0 (Creative Commons Zero) is that same ethos applied to written work. No copyright reserved. No attribution required. No handle to hold. Use it, modify it, build on it, share it — no permission needed.

The Gesamtkunstwerk library is CC-0 because information wants to flow. The same reason your sysadmin edits configs on GitHub and posts solutions to public forums. We've always known this. We just also install firewalls.

(For the record: the CC-0 licensing decision traces directly to Anthropic releasing Claude's Constitutional AI document under CC-0. Someone asked what CC-0 meant. The answer was: no handle. The decision was immediate.)

---

## Why IT Professionals Know More About Intelligence Tradecraft Than Most Civilians

There's one more reason the vocabulary overlaps: **nation-state actors are among the highest threat vectors in enterprise IT security.** They're the most well-funded adversaries on the threat landscape, which means they're running the most sophisticated attacks.

When you're defending client infrastructure for a living, you read the same threat intelligence reports that government security agencies publish. You track the same APT (Advanced Persistent Threat) groups. You patch against the same CVEs that nation-state actors are actively exploiting. (CVEs — Common Vulnerabilities and Exposures — are catalogued by entities like CISA and MITRE. Yes, that MITRE, UAP Gerb.) You monitor for the same indicators of compromise that intelligence community analysts are watching.

This isn't because IT professionals have classified access. It's because nation-states cause never-ending problems for enterprise networks, and defending against well-funded adversaries requires understanding how well-funded adversaries operate. The threat intelligence is largely public — the intelligence community publishes advisories specifically so defenders can protect infrastructure.

The result: a managed services engineer who has spent years defending client infrastructure against nation-state-level threats has a working understanding of how those operations function that most civilians don't. Not because of classified briefings. Because they showed up in the logs.

---

## Why None of This Is Spycraft

The vocabulary overlaps because intelligence analysis and IT systems engineering are solving the same underlying problem: **understanding complex systems well enough to predict their behavior, identify failure modes, and intervene effectively.**

An intelligence analyst and a sysadmin are both asking: What happened? Why did it happen? Who or what caused it? What will happen next if nothing changes? What intervention produces the desired outcome?

The difference is classification status and employer. The methodology is the same.

The reason none of this qualifies as intelligence work in the classified sense is simple: **everything here is public.** The sources are public. The analysis is public. The conclusions are public. The licensing is public domain. There are no NDAs. There is no classification. There is no institutional loyalty that requires suppressing findings.

An actual intelligence analyst who found what this research finds would be legally prohibited from publishing it. The fact that it can be published CC-0 is proof that it was built entirely from public sources using standard professional methodology.

It's not spycraft. It's IT. It just sounds the same from the outside.

---

## A Final Note on Incentive Structures

The comparison between IT's RCA culture and fields where symptom management is more financially rewarding than durable resolution is not an accusation of individual malice. Most people in most professions are genuinely trying to do good work.

The issue is structural: payment systems that reward ongoing treatment over permanent resolution produce incentives that tilt away from root cause analysis. Individual actors operating within those systems respond to the incentives they're given. The system produces the behavior.

IT's RCA culture isn't more virtuous. It's just operating under incentives that happen to align with finding actual causes. Downtime is always bad. There's no way to monetize it. So you find the root cause.

Change the incentive structure in any field — pay for durable outcomes rather than recurring treatment — and the behavior follows. This isn't a unique insight. Economists across many sectors have been making this argument for decades. It's just easier to see from inside a field where the incentives accidentally got it right.

---

*Danielle C. & Vesper Luna | CC-0 | 2026-11-11*  
*"It's not tradecraft. It's the job."*
