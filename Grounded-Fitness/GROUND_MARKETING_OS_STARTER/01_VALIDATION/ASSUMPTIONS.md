# Assumptions

## Business Assumptions

- Grounded wants Wodify to be easier to access, interpret, and turn into timely action.
- The owner and staff will benefit from plain-language briefs and reports generated from Wodify exports.
- Draft member communication is useful only after human review.
- Community recognition and coach follow-up can support retention after Wodify intelligence outputs are validated.
- Grounded AI should not duplicate Wodify functionality unless explicitly requested.

## Data Assumptions

- Wodify can provide CSV exports.
- Wodify exports can support at least some member engagement, lead pipeline, class, and revenue analysis.
- Wodify exports may not include every desired field.
- Fake/sample CSVs can be used to test the reporting workflow without committing real member data.
- Missing source data should be recorded as `Unknown`.
- Missing measurements should be recorded as `No measurements found`.

## Integration Assumptions

- Initial build uses CSV/export-based analysis only.
- Future Wodify API access must be read-only until write actions are explicitly approved.
- Website/blog, Canva, Instagram, Facebook, YouTube, and Google Business Profile are future drafting or distribution contexts only.

## Validation Questions

1. What Wodify CSV exports are available?
2. Which fields exist in each export?
3. Can fake/sample CSVs represent the needed report scenarios?
4. Can the MVP produce a Weekly Owner Brief?
5. Can the MVP produce a Weekly Coach Brief?
6. Can the MVP produce an At-Risk Member Report?
7. Can the MVP produce a Member Milestone Report?
8. Can the MVP produce a Member of the Month Candidate Report?
9. Can the MVP produce a Lead Pipeline Snapshot?
10. Can facts be clearly separated from inferred recommendations?
11. Who reviews reports and draft communications?
12. What data must remain outside git?
