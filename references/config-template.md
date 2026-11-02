# Recruiting Outreach Configuration

Copy this template into your own private project/folder and complete every required field. Leave no bracketed placeholders. Use `none` or `[]` for unused lists. Keep the shared skill unchanged. Supply your completed configuration when invoking Recruiting Outreach.

## Run identity and permissions

- Configuration ID: [unique campaign label]
- Create Gmail drafts: [yes or no]
- Paid lookup spending authorized: [yes or no; no when tool is none]

Authorize drafts only. The skill never sends mail or schedules actual sends. Recurring automation requires separate setup.

## Me

- Full name: [full name]
- Email: [email]
- Phone: [phone]
- School: [university and school within it]
- Degree and year: [degree and graduation year]
- Standing: [current standing, such as third-year undergraduate]
- Focus: [major, concentration, minors]
- University and city: [university, city]
- LinkedIn URL: [full profile URL]

## Output

- Report destination: [private project/folder path or supported destination link]
- Send-schedule time zone: [IANA zone, such as America/New_York]
- Schedule start time: [local time, such as 09:00]

## Lookup

- Address-verification tool: [tool name or none]
- Maximum credits per run: [nonnegative integer; 0 when none]
- Current credit balance: [nonnegative number or not applicable when none]
- Balance checked on: [YYYY-MM-DD or not applicable when none]
- Warn below: [nonnegative threshold; 0 when none]

Connect the selected tool before running it. It must return an explicit verification status. Unknown patterns never authorize guessing an address.

## Contact volume

- Cumulative cap per exact role/program/practice and location: [positive integer]

Count distinct prior cold contacts and active cold drafts for this configuration. Warm replies do not consume new cold slots.

## Exclusions

Use `[]` if empty. Exclusions include subdomains and apply to warm contacts too.

| Domain | Reason |
| --- | --- |
| [domain] | [reason] |

## Target roles: priority 1

Use stable target IDs. Name the exact program, year, location, and practice if relevant. Use `[]` for an empty list; at least one priority list must contain a target.

| Target ID | Firm | Exact program and year | Location | Practice or narrowing notes |
| --- | --- | --- | --- | --- |
| [P1-01] | [firm] | [program/year] | [city/office] | [undergraduate vs MBA, practice, or none] |

## Target roles: priority 2

| Target ID | Firm | Exact program and year | Location | Practice or narrowing notes |
| --- | --- | --- | --- | --- |
| [P2-01] | [firm] | [program/year] | [city/office] | [notes or none] |

## Target domains

Map every target firm. Include confirmed employee email domains and legacy aliases. Supply reliable evidence or let setup verify the mapping before drafting. Never guess from the firm name.

| Firm | Email domain(s) | Evidence/source and date |
| --- | --- | --- |
| [firm] | [comma-separated domains] | [source/date] |

## Seed list

List people already contacted who might not appear in sent mail. Use `[]` if empty.

| Name | Email | Firm | Status and date if known |
| --- | --- | --- | --- |
| [name] | [address] | [firm] | [sent/replied/bounced/chat-completed, date] |

## Known warm contacts

Include former target firms when follow-up is useful. Current threads take precedence. Use `[]` if empty.

| Name | Firm | Email or domain | Outstanding offer/action |
| --- | --- | --- | --- |
| [name] | [firm] | [address/domain] | [offer or next step] |

## Initial address-pattern evidence

Use `[]` for no evidence. Do not copy another user's patterns or bounce totals. The skill maintains later findings in private run reports.

- Historical constructed-address hard-bounce total: [known number with evidence, or unknown]

| Domain | Policy: unknown / verify-only / safe-to-construct / do-not-construct | Exact rule | Examples and provenance | Catch-all evidence | Constructed-address hard bounces and evidence |
| --- | --- | --- | --- | --- | --- |
| [domain] | [policy] | [rule or unknown] | [verified/published/inbound source/date, or none] | [source/date or unknown] | [count/source/date or unknown] |

Mark safe-to-construct only when you deliberately accept an evidenced rule. A conflicting rule or constructed-address hard bounce stops construction. Catch-all domains require verified or published addresses.
