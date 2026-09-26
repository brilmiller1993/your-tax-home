# Marketing Training & Outreach Workspace

## Product requirement

Add a tenant-aware Marketing Training & Outreach workspace to every white-label company account in Your TAX HOME. It must use the existing account, branding, authentication, storage, and role model. Do not create a standalone marketing company, sample customer, or replacement app.

The workspace must be available to each white-label account and branded from that account's saved company name, logo, and brand colors. Do not hardcode another company's name or any city/state in page copy, forms, agreement defaults, sample data, or rate labels. Use the current white-label company's brand in generated agreements, forms, reports, and employee-facing pages. If an employee enters a preferred city or work location, show the employee-entered value only to that employee and authorized admins in the same tenant.

The current repository's HTML prototype stores demo data in browser localStorage. This feature needs shared, durable, authenticated storage. Connect it to the project's existing backend and follow its current framework and data conventions. Do not treat localStorage, a mock API, or a success message as a saved upload or cross-user report.

## Roles and access flow

1. Add a **Marketing Team Member** application path to the existing role/package signup flow. Applicants may enter the marketing workspace request before approval, but must not see internal training, company records, partner data, employee documents, or admin reports.
2. Create an application status flow: **Submitted → Under review → Approved / Not approved**. Show a clear status page to applicants.
3. A tenant admin reviews applications and may approve or decline, set a supervisor, choose the initial position, approved hourly rate or production arrangement, scheduled-hours cap, and the employee's first assigned checklist/training track.
4. Do not unlock marketing tools or records until the tenant admin approves the applicant and assigns at least one position. Once approved, show only the employee's assigned work, training, forms, and records.
5. Tenant admins can assign, change, or remove positions and can assign a different track to each employee. Log approvals, assignments, rate changes, document decisions, and status changes.
6. Enforce tenant isolation on the server/database and file storage. An admin can view records only for their own white-label company. Employees can see only their own application, training progress, assigned tasks, submitted reports, and permitted team items. Never rely on hiding a menu item alone for authorization.

## Marketing and outreach positions with reusable pay bands

Show the following pay ranges without naming or implying a city, state, or region. Label the columns **Range A** and **Range B**. These are display ranges; a tenant admin must choose the actual rate or compensation arrangement for an individual assignment.

| Position | Range A | Range B |
| --- | --- | --- |
| Flyer Distributor / Street Team | $18–$20/hr | $20–$22/hr |
| Sign Holder / Brand Ambassador | $18–$20/hr | $20–$22/hr |
| Social Media Promoter | $20–$23/hr | $22–$25/hr |
| Community Outreach Representative | $20–$25/hr | $22–$27/hr |
| Client Acquisition Representative | $20–$25/hr + incentives | $22–$27/hr + incentives |
| Tax Preparer | $22–$30+/hr or production-based | $24–$32+/hr or production-based |
| Lead / Senior Tax Preparer | $28–$35+/hr | $30–$38+/hr |

Allow applicants to select a desired position, enter their desired pay within or outside the displayed range, set availability, and enter their desired city, neighborhood, or other preferred work location as free text. Do not show city/state suggestions prefilled by this document. The admin sets the approved rate and schedule. Display pay-band guidance as informational, not a promise of hours or a job offer. Before saving an approved rate, show an admin reminder to verify the applicable wage rules for the employee's work location.

The schedule field must support the supplied startup limit: **up to 4 scheduled hours per biweekly pay period unless management approves additional hours and applicable law allows them.** Track actual hours worked accurately. Do not use photo/GPS verification to deny wages for compensable time.

## Employee application and onboarding forms

Create a mobile-friendly application with these fields:

- Full name, email, phone, and preferred contact method
- Desired position(s)
- Relevant experience, skills, languages, and short introduction
- Availability by day/time and preferred start date
- Desired pay
- Desired city / neighborhood / locations to work (employee-entered free text)
- Optional resume or relevant work sample upload
- Agreement to follow approved marketing, privacy, safety, and conduct rules
- Consent for the specific outreach verification fields the tenant enables

After approval, the admin can require and assign documents such as a signed worker agreement, signed marketing/privacy acknowledgment, training completion evidence, approved work sample, or other tenant-approved onboarding document. Make each item optional/required per tenant policy. Use private storage with access checks and file type/size validation. Never place uploaded files on a public URL. Do not request or accept taxpayer tax documents, Social Security numbers, bank credentials, IRS credentials, or customer financial records in this marketing area.

## Marketing training

Add an employee-facing training area with position-specific tracks and progress. Initial modules should cover:

- Representing the white-label company accurately and using approved brand materials
- Respectful flyer, sign, event, and business outreach
- How to introduce a referral program using only approved terms
- How to record leads and business-partner follow-ups
- Privacy, consent, and what information must never be collected in outreach
- Safe outreach, property rules, de-escalation, and incident reporting
- Photo and activity-report standards
- Approved social content, claims, and escalation for questions
- Time reporting and schedule expectations
- Knowledge checks and acknowledgment of company policies

Allow the tenant admin to assign or lock/unlock modules by employee or position. Show completion status to that tenant's admins. Training materials must dynamically use the tenant brand; do not use the sample employer's name or geography.

## White-label street team agreement

Provide an editable, tenant-branded agreement template, rendered with the current white-label company's name, logo, colors, selected worker, assigned position, supervisor, start date, admin-approved rate, scheduled-hours limit, and employee-entered preferred work area. Do not include a prefilled city or state. Allow the admin to review, edit tenant-specific text, preview, generate a downloadable copy, and request an employee acknowledgment/signature. Store the signed version and version/date audit history privately. Mark it as a business template for legal review before tenant use.

Use the following terms as the initial editable template language, replacing every named sample-company reference with the current tenant's dynamic company name:

### STREET TEAM EMPLOYEE / WORKER AGREEMENT

**Company:** {{tenant.company_name}}  
**Worker name:** {{worker.full_name}}  
**Position:** {{worker.assigned_position}}  
**Start date:** {{employment.start_date}}  
**Supervisor:** {{employment.supervisor}}  
**Preferred work area (entered by worker):** {{worker.preferred_work_location}}  
**Approved pay rate:** {{employment.approved_rate}}  
**Scheduled hours:** Up to 4 scheduled hours per biweekly pay period unless otherwise approved by management and subject to applicable law.

#### 1. Purpose of position

The representative assists {{tenant.company_name}} with community outreach, marketing, brand awareness, lead generation, and business partnership development.

The representative may be assigned to:

- Hold company-approved promotional signs.
- Distribute flyers and business cards.
- Promote {{tenant.company_name}} in approved public or private locations.
- Visit businesses to introduce the company and seek potential referral partnerships.
- Identify dealerships, grocery stores, salons, retail businesses, community organizations, and other businesses that may be appropriate referral partners.
- Collect approved business contact information.
- Follow up with potential business partners as directed.
- Track businesses contacted and partnerships pursued.
- Generate qualified individual and business referrals.
- Follow all company marketing, privacy, safety, and professionalism requirements.

#### 2. Assigned outreach activities

**Sign holding / public outreach.** When assigned sign-holding duties, the representative must remain in the approved outreach area and actively perform the assignment. This may include parking in an appropriate location, exiting the vehicle when required, holding the approved sign, remaining visible, distributing approved materials when appropriate, and following property-owner rules. Paid promotional time is not for personal errands, sleeping, leaving the assigned area without authorization, or remaining inside a personal vehicle when the assignment requires active outdoor promotion.

**Business outreach.** When assigned to business outreach, the representative should make reasonable efforts to visit at least two business establishments during the scheduled outreach period when feasible and consistent with the assigned schedule. Potential businesses may include car dealerships and automobile lots, grocery stores, salons and barbershops, clothing stores, apartment communities, insurance offices, real-estate offices, small businesses, community organizations, and other businesses approved by management. Representatives may introduce the company, provide approved materials, explain the referral program using company-approved information, and request the appropriate contact person for follow-up.

Representatives may not independently negotiate contracts, change referral amounts, make promises on behalf of the company, or sign agreements unless specifically authorized.

#### 3. Time, location, and activity verification

The company may use reasonable procedures to document outreach activity and accountability.

At the beginning of an assigned outreach period, the representative may be required to record the actual start time, identify the assigned location, and submit a current arrival photo showing the representative at or near the outreach location and, when appropriate, the activity.

During scheduled outreach, the representative is expected to perform the assigned duties, such as holding the approved sign, distributing flyers, speaking with potential customers or business partners, collecting approved business contact information, and completing assigned reports.

At the end of an assigned outreach period, the representative may be required to record the actual end time, submit a current departure photo showing presence at or near the location and/or completion of the activity, and complete the required outreach report.

Photos and activity records are intended to establish reasonable evidence of **time, location, and activity**. The company may request additional documentation when necessary. GPS/location collection, if enabled, must be disclosed and requested only for the assigned activity under the tenant's approved policy; do not collect background location.

#### 4. Verification is not a substitute for legally required timekeeping

Verification procedures document accountability and verify time, location, and activity. Photos, GPS/location information, sign-holding photos, activity reports, and other verification materials do not replace legally required timekeeping, payroll records, meal/rest requirements, or other wage-and-hour obligations.

Representatives must accurately report all time actually worked. Failure to provide a required photograph does not automatically forfeit wages legally owed for compensable time worked. Failure to follow reasonable verification procedures may result in a request for additional documentation, assignment review, or other appropriate action subject to applicable law. The company will maintain required employment and payroll records as applicable.

#### 5. Photo requirements

When photos are required, they must be taken during the assigned period, truthfully and currently, and reasonably show presence at the assigned location and/or activity. Reused, altered, misleading, or falsely presented photos are prohibited. Representatives must not photograph tax documents, customer financial information, Social Security numbers, identification documents, or other confidential information. Representatives must respect property rules and privacy expectations.

#### 6. Business contact tracking

For each business contacted, record the business name, business type, address/location, contact person or role, approved phone/email, date contacted, whether a partnership was requested, whether follow-up is needed, next follow-up date, and result. Submit business outreach information according to the company's reporting schedule.

#### 7. Referral program

The company may offer incentives under its approved referral program. A qualified business referral may result in a **$100 referral incentive** when all company requirements have been met and the referred client actually files through {{tenant.company_name}}. A qualified individual referral may result in a **$50 referral incentive** when all company requirements have been met and the referred client actually files through {{tenant.company_name}}.

Referral incentives are subject to verification, company approval, applicable law, and referral procedures. A lead, inquiry, call, appointment, or business introduction alone does not guarantee payment.

#### 8. Referral requirements

A referral generally must be submitted through the approved process, identify the referring representative/business/individual, be a legitimate new referral, be documented by the company, result in a new client who actually files through {{tenant.company_name}}, and satisfy company and legal requirements. No incentive is guaranteed for duplicate or unverifiable referrals; existing clients improperly submitted as new; leads that never file; cancelled or abandoned matters; fraudulent, self-created, or manipulated referrals; or referrals that violate policy or applicable law.

#### 9. Professional conduct

Representatives must treat customers and businesses respectfully; represent the company truthfully; use only approved marketing materials; avoid false or misleading statements; never guarantee a refund or promise approval for a credit, loan, grant, or financial product; never provide unauthorized tax advice; never collect confidential taxpayer information unless specifically authorized and properly trained; follow property-owner rules; avoid harassment, aggressive solicitation, or confrontational conduct.

#### 10. Company materials

Company signs, flyers, business cards, promotional materials, scripts, forms, logos, and other materials remain company property unless otherwise stated. Return company property when requested.

#### 11. Confidentiality and client privacy

Representatives may encounter confidential business or customer information. They must not share customer information, photograph tax documents, post confidential information online, sell or distribute company leads, use customer information for personal business, or disclose private company information to unauthorized persons. These obligations continue after the representative's work with the company ends.

#### 12. Safety

Representatives should use reasonable safety practices. They should not enter unsafe areas, confront hostile individuals, trespass, remain after authorized property personnel instruct them to leave, or place themselves in unnecessary danger. Report safety concerns to management as soon as reasonably possible.

#### 13. Pay and time reporting

The representative must accurately record all time worked. The company will process wages according to the applicable payroll schedule and applicable federal, state, and local requirements. Incentive or referral payments will be handled separately under the approved program and required tax/payroll reporting rules.

#### 14. No unauthorized commitments

Representatives may not change company pricing or referral amounts; promise refunds or tax results; sign contracts without authorization; commit the company to a partnership without management approval; promise employment, grants, or loans; or promise a specific tax outcome.

#### 15. Acknowledgment

By signing below, the representative confirms that they have received and reviewed the agreement and understand the responsibilities associated with the assigned position.

**Worker name:** {{worker.full_name}}  
**Worker signature / acknowledgment:** {{worker.signature}}  
**Date:** {{worker.signed_at}}  
**Company representative:** {{tenant.authorized_representative}}  
**Signature:** {{tenant.representative_signature}}  
**Date:** {{tenant.representative_signed_at}}

*This document is a business template and must be reviewed by the tenant for applicable employment, tax-preparer, advertising, privacy, and other legal requirements before use.*

## Employee activity forms

Build real forms that save to the tenant database and show submitted/saved status only after the backend confirms success:

### Outreach shift report

- Assigned campaign/shift and assigned position
- Actual start and end time; unpaid/paid breaks and total actual time worked as required by the tenant's timekeeping policy
- Date and worker-entered location/service area
- Activity type: sign holding, flyer distribution, business visits, community event, social promotion, client acquisition, or other admin-approved type
- Flyers/business cards distributed (numeric count)
- Businesses/organizations visited and outcome
- Leads/referrals generated (link to separate referral record; no tax facts or tax documents)
- Photo/document upload when required
- Safety issue or notes
- Worker attestation that entries are truthful and current
- Admin review status and reviewer notes

### Business partnership / business-contact form

- Business name and type
- Employee-entered address/location or service area
- Contact name, role, phone/email (collect only business contact details needed for follow-up)
- Date contacted, outreach method, materials provided
- Partnership requested: yes/no
- Follow-up needed: yes/no; due date
- Result/status: contacted, follow-up, interested, requested agreement, submitted for approval, approved/active, declined, or inactive
- Proposed partner/referral terms (display approved standard terms; employee cannot change them)
- Notes and optional business card/approved documentation upload
- Admin decision, assigned follow-up owner, and timestamps

Track separately the number of businesses contacted, partnership requests, approved/active partnerships, and partners that have produced qualified referrals. Do not count a simple contact as an obtained partnership.

### Referral / lead form

- Referral type: business or individual
- Referrer employee/partner
- Referred contact name and permitted contact details, with consent/permission confirmation
- Referral date, source/campaign, and follow-up owner/status
- Client conversion/filed status visible only to authorized admin/preparer roles
- Incentive eligibility and payment status controlled by admins; do not expose taxpayer records to marketing staff
- For a qualified completed business referral, show the configured $100 base incentive; for a qualified completed individual referral, show the configured $50 base incentive. Admin may edit a tenant's program; all changes need a dated audit record. Do not auto-pay an incentive just because a lead was submitted.

Do not put return data, documents, income, dependents, SSNs, refund amounts, or tax-preparation notes in marketing records. Provide a secure, role-approved handoff to the tax office for client intake.

## Tenant admin reporting and management

Add an admin-only Marketing overview and detail views, scoped to that tenant. Include date range and position filters and export of permitted columns to CSV. Provide these summary metrics:

- Applications submitted, awaiting review, approved, and not approved
- Active marketing employees by assigned position
- Businesses contacted, partnership requests, approved/active partnerships, and follow-ups due/overdue
- Qualified individual/business referrals, conversion/filed totals, pending review, and incentive totals/status
- Outreach shifts and actual hours by employee, position, campaign, date, and employee-entered service location
- Sign-holding time and completed shifts
- Flyer/business-card counts, event attendance, and social promotion activity
- Missing or pending agreement/document/training items
- Outreach records returned for correction and safety incidents requiring review

Provide drill-down to the underlying records, with permission-aware filters. Display work location as employee-entered; do not map or insert preset locations from this document. Reports should answer how many partnerships were obtained, where teams were assigned/serviced, whether flyers were promoted or signs held, and for how long. Keep payroll/time records separate from optional photo evidence and never compute hours solely from photos or location signals.

## Suggested backend entities

Adapt names to the existing schema rather than duplicating existing user/account tables:

- marketing_applications: tenant_id, user_id, contact/application fields, desired_positions, preferred_locations, availability, desired_rate, status, reviewer, review timestamps
- marketing_assignments: tenant_id, user_id, position, approved_rate, compensation_type, supervisor_id, schedule_cap, active status, assigned_by, timestamps
- marketing_training_modules and marketing_training_progress: tenant-owned module assignment/locks and per-user completion/quiz/acknowledgment
- marketing_documents: tenant_id, user_id, document_type, private_storage_key, status, reviewer, timestamps, agreement_version
- outreach_shifts: tenant_id, user_id, campaign_id, activity type, actual time fields, employee-entered service area, counts, notes, review status
- outreach_media: tenant_id, shift_id, private_storage_key, uploaded_by, capture time, reviewer status
- business_partners: tenant_id, created_by, business/contact fields, outreach status, follow-up dates, approval audit fields
- marketing_referrals: tenant_id, created_by, referral type, permitted referral contact fields, source, status, client conversion/filed verification flags, incentive status
- marketing_audit_events: tenant_id, actor_id, action, target type/id, timestamp, safe change summary

Add indexes for tenant, status, assigned employee, activity date, and follow-up date. Add row-level authorization and private object-storage rules for every tenant-owned table/object. Use minimal PII and prevent marketing-role reads of tax-return or taxpayer data.

## Acceptance checks

- A new marketing applicant can submit an application and sees only its review status.
- An admin of one white-label account cannot view or change another account's employees, partners, uploads, or reports.
- Approval plus position assignment unlocks only the assigned employee workspace and checklist.
- Admin can choose a different first position for different workers; the worker sees the matching training and tasks.
- Worker can submit a shift report, partner record, referral, and permitted upload; another authenticated team member/admin sees the saved records only if their tenant role permits it.
- Admin report counts distinguish contacted businesses from approved partnerships and distinguish leads from qualified/filed referrals.
- Worker can enter their preferred city/location and actual service location without any preset city/state in the template.
- White-label name, logo, and colors appear in the employee workspace and generated agreement. No sample company's name or preset city/state appears in any visible UI or default document text.
- The listed pay ranges and referral incentives are present, while actual approved rates and tenant changes are audited.
- Actual time reporting remains available if photos are missing; photos are supporting evidence only.
- Build and run the app's relevant checks, exercise each role and tenant boundary, and verify uploads use private authenticated storage before publishing.
