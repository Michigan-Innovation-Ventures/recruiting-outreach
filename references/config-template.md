# Recruiting Outreach Configuration

Copy this file to your private destination (outside the skill) and complete every field. Bracketed placeholders count as missing. Use `none` or `[]` only where the field says it is allowed. Never commit a completed copy to the shared skill.

## 1. Campaign

- configuration_id: [unique ID, for example `fall-2026-consulting`]
- draft_target: [positive integer, default 50 new cold drafts per run]
- draft_creation_authorized: [yes or no. Must be yes to create drafts]

## 2. Identity (used in drafts)

- full_name: [First Last]
- first_name: [First]
- school: [University of Michigan]
- standing: [Sophomore, Junior, and so on. Used in the subject and body]
- degree_and_year: [for example BSE Computer Science, Class of 2028]
- focus: [major or field as it should read in "studying ..."]
- university_and_city: [University of Michigan, Ann Arbor, MI]
- email: [school email]
- phone: [phone number]
- linkedin_url: [full LinkedIn profile URL]
- resume_file: [path to resume file the draft tool can attach, or `none`]
- resume_link: [public resume URL, or `none`]

## 3. Run settings

- report_destination: [private folder or connector location the run can read and write]
- time_zone: [IANA zone, for example America/New_York]
- schedule_start_time: [local time for first proposed slot, for example 09:00]

## 4. Targets

One entry per exact firm, program, year, practice, and location. Priority 1 runs before priority 2.

```text
- id: [short unique ID]
  priority: [1 or 2]
  firm: [exact firm name]
  org_type: [large firm or startup]
  program: [exact program, for example Summer Analyst]
  year: [program year]
  practice: [practice or team, or `any`]
  location: [city or office]
  cumulative_contact_cap: [positive integer of distinct people across all prior and new cold outreach]
```

backfill_targets: [list in the same format as above with priority 3, or `[]`. Used only after priority 1 and 2 are exhausted]

## 5. Domains

Confirmed firm-to-domain mappings. Include documented legacy domains after acquisitions. Unresolved mappings are skipped.

```text
- firm: [exact firm name]
  domains: [domain one, domain two]
```

excluded_domains: [domains never to contact, including warm replies, or `[]`]

## 6. Seed contacts and history

- seed_do_not_contact: [addresses to never cold-email, or `[]`]
- prior_replied_bounced_chat_completed: [addresses with status, or `[]`]
- known_warm_contacts: [addresses or domains to check for warm threads, or `[]`]

## 7. Email lookup

- lookup_tool: [tool name, or `none`]
- per_run_max_spend: [credits or dollars]
- balance_checked: [amount and date]
- warning_threshold: [balance at which the report must warn prominently]

## 8. Address ledger

Start new campaigns with unknown patterns. Do not copy another campaign's ledger.

```text
- domain: [domain]
  rule: [observed pattern, or `unknown`]
  evidence: [exact address, source, date]
  safe_to_construct: [yes or no]
  catch_all: [yes, no, or unknown]
  hard_bounces: [count observed, or `unknown`]
```

- historical_hard_bounce_total: [number, or `unknown`]

## 9. Carryover

- exhausted_searches: [target ID, search URL, date, reason, or `[]`]
- unknown_domain_holds: [domain and last actual send time, or `[]`]
