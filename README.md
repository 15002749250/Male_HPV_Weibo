# Male HPV vaccination discourse on Weibo: research data and documentation

Title: **Negotiating trust, responsibility and gender in male HPV vaccination on Weibo**  

**Repository:** https://github.com/15002749250/Male_HPV_Weibo

## 1. Study and data overview

The study uses corpus-assisted critical discourse analysis to examine public Weibo discussions following the expansion of HPV vaccine eligibility to males in mainland China in January 2025. Publicly accessible material was retrieved on **4 September 2026** using the Chinese keyword corresponding to “male HPV vaccine” and 23 relevant trending hashtags. The comment observation period is **8 January 2025 to 3 September 2026**. Retrieval is conditional on the search strategy and platform visibility; the collection is not an exhaustive or population-representative sample.

| Dataset or sample | Size | Analytical role |
| --- | ---: | --- |
| Source corpus | 23,609 comments linked to 443 parent-post records | Screening provenance, comment-level descriptive context and overall like statistics |
| Screened analytic corpus | 18,246 retained comments | Descriptive mapping of stored, overlapping category indicators |
| Qualitative sample | 20 purposively selected discussion episodes, with 3,732 source comments | Contextual reading of parent posts and comments |
| Retained comments within the 20 episodes | 3,133 | Subset used for substantive qualitative interpretation |
| Excluded comments within the 20 episodes | 599 | Preserved for examination of screening decisions; not used as substantive qualitative evidence |

The 3,133 retained episode comments are **already included** in the analytic corpus of 18,246 comments. Episode comments are not an additional dataset to add to the analytic total. Parent posts provide context and are **not counted** as comments.

## 2. Repository contents

| File | Content and worksheets |
| --- | --- |
| `Source_Corpus.xlsx` | `Source_Corpus`: 23,609 comment records with de-identified text and recorded metadata. `Parent_Posts`: 443 linked contextual parent-post records. `Screening_Flow`: exclusion steps and counts. `Documentation`: data-processing notes. |
| `Analytic_Corpus.xlsx` | `Analytic_Corpus`: 18,246 retained comments and recorded analysis fields. `Frame_Audit`: summaries of A–N category labels and examples. `Topic_Lexicon`: 130 terms used for off-topic screening. `Documentation`: data-processing notes. |
| `Qualitative_20 Episodes.xlsx` | `Episodes`: 20 episode-level descriptors and contextual parent-post text. `Episode_Comments`: 3,732 comment records, including both retained and excluded records. `Documentation`: data-processing notes. |
| `Domain_Lexicon.csv` | The 130-term screening-domain lexicon; **not** the complete set of A–N category matching rules. |
| `Category_Examples.csv` | Recorded A–N categories, their documentation crosswalk, and **illustrative keyword examples only**. Examples are not complete coding or matching specifications. |
| `Additional_Aggregates.xlsx` | `Corpus_Flow`, `Category_Frequencies`, `Monthly_Volume`, `Episode_Summary`, and `Overall_Engagement`: supporting descriptive summaries. |
| `README.md` | This documentation, including corpus relationships, known limitations and ethical safeguards. |

The separate **Supplementary Table S1** in the manuscript reports aggregate overall engagement statistics; it does not contain individual-level records. The repository's `Overall_Engagement` worksheet supplies related descriptive values.

## 3. Relational structure and important fields

The public files use newly assigned **package-specific record keys**, not original Weibo account identifiers:

- `comment_id` (prefix `C`): comment-level key. Join individual comments between the source corpus, analytic corpus and episode sample using this field.
- `post_id` (prefix `P`): key identifying a parent-post record. Use it to connect comments with `Parent_Posts` or episode information.
- `source_account_id` (prefix `S`) and `commenter_id` (prefix `U`): reassigned keys for recorded account relationships. These are not original platform identifiers or username hashes; they do not establish demographic identity.
- `episode_id` (prefix `E`): identifier for a purposively selected discussion episode, E1–E20.
- `screening_status`, `exclusion_step` and `exclusion_reason`: recorded screening outcomes and the step at which an exclusion was applied.
- `comment_text_deidentified` and, where applicable, `comment_text_clean_deidentified`: de-identified textual fields. Cleaned text is not necessarily identical to the original export.
- `comment_date`, `year_month` and `phase`: temporal reference fields. **The date precision has been reduced to the calendar day.** A displayed value such as `2025-01-08T00:00:00.000Z` is a date-normalisation representation, **not** a verified time of posting.
- `like_count`, `reply_count`, `floor_number` and `source_order_in_post`: recorded engagement and export-context fields. `source_order_in_post` follows spreadsheet/export order; it is **not** a verified chronological order or reply-to sequence.
- `record_link_status`: recorded status of linkage where matching was uncertain. Ambiguous links should not be treated as verified person-level matches.
- `frame_codes_recorded`: stored, potentially **overlapping** A–N lexical-category labels. A comment can have more than one label or none. These values are descriptive indicators, not a mutually exclusive classification of comments or respondents.
- `redaction_applied` and `clean_redaction_applied`: flags recorded during de-identification processing. A zero flag does not guarantee that a passage is unsearchable or that no indirect identification risk remains.

The dataset preserves the historical processing record; field names containing “recorded” signal information taken from the supplied analysis and its audit documentation rather than from a new complete reclassification.

## 4. Screening from source to analytic corpus

The exclusion steps were applied sequentially, with the remaining count after each step shown below.

| Step | Recorded rule | Excluded at step | Remaining |
| --- | --- | ---: | ---: |
| Start | Source comments | — | 23,609 |
| X1 | Empty text | 0 | 23,609 |
| X2 | Platform-generated messages | 2 | 23,607 |
| X3 | No substantive language after cleaning, including emoji-, link- or mention-only material | 1,220 | 22,387 |
| X4 | Exact duplicate text by the same recorded user | 542 | 21,845 |
| X5 | Templated promotional content | 2,425 | 19,420 |
| X6 | Off-topic material under the recorded lexical rule | 1,174 | 18,246 |
| **Total** | **Excluded records** | **5,363** | **18,246** |

The documented X5 promotional rule used a repetition frequency of **at least 10** and a mean like count **below 5**. The documented X6 off-topic rule used **zero matches** against the 130-term domain lexicon, a recorded cleaned-text length **of at least 15**, and **fewer than 10 likes**. Like counts thus entered two screening decisions, potentially influencing the composition of the analytic corpus. The provided workbooks document these outcomes but do not include all historical processing scripts.

Repetition alone was not grounds for removing meaningful comments in the narrative interpretation. The source corpus retains excluded records for checking the screening flow.

## 5. Descriptive mapping and interpretation

The analytic corpus contains stored A–N indicator labels for topics, orientations, strategies and identity-related language. The `Frame_Audit` worksheet and `Category_Examples.csv` document the labels and sample keywords. **Their examples are incomplete and do not reconstruct the original full A–N matching rules.** The conceptual four-level crosswalk is an aid to interpreting the stored labels, not four separately validated coding schemes.

Counts in `Category_Frequencies` refer to recorded, overlapping indicator matches among **18,246** retained comments. **8,947** retained comments have no recorded category label. Therefore, category counts do not estimate the complete prevalence of a discourse or the proportion of Weibo users holding a position. They cannot be interpreted as support, hesitation or uptake rates.

Twenty parent-post/comment episodes were purposively selected to vary posting-account type, observation phase, acceptance and contestation, and engagement context. The sample includes strongly affirmative, explicitly refusing and less-engaged contrasts. The dataset does not establish a complete reply-to network. Textual response markers and available parent-post context were used to interpret claims; comment ordering alone is insufficient to infer a conversational sequence or changes in a person's views.

## 6. Observation phases and engagement summaries

The four descriptive phases organize sampling and monthly counts; their boundaries do **not** support causal claims about approval or promotional events:

| Phase | Calendar period | Source comments |
| --- | --- | ---: |
| Phase 1 | January–March 2025 | 6,034 |
| Phase 2 | April–December 2025 | 8,805 |
| Phase 3 | January–April 2026 | 4,488 |
| Phase 4 | May–3 September 2026 | 4,282 |

`Monthly_Volume` records calendar-month counts; September 2026 includes observations **only through 3 September**.

`Overall_Engagement` summarises the distribution of `like_count` across **all 23,609 source comments, before screening**, including zero-like records. This is **descriptive**: likes depend partly on exposure and cannot establish agreement, representativeness, actual influence or algorithmic amplification. The reported 99th percentile uses linear interpolation, and `ln1p_likes` is the natural logarithm of `1 + like_count` for each comment. The published analysis does **not** infer differences in engagement among A–N categories from this worksheet.

## 7. Suggested checks of the reported results

Readers can use the files to independently examine the following documented quantities:

1. Count all rows excluding the header in `Source_Corpus` and compare with 23,609; check that the `Screening_Flow` exclusions total 5,363 and leave 18,246.
2. Count retained comments in `Analytic_Corpus` and use `frame_codes_recorded` to check stored, nonexclusive A–N category frequencies against `Category_Frequencies`. Keep the full analytic corpus as the denominator, including unlabelled rows.
3. Group source `year_month` values to compare with `Monthly_Volume`, recognising that this is a description of the retrieved corpus rather than of all Weibo activity.
4. In `Episode_Comments`, group by `episode_id` and `screening_status` to compare with `Episode_Summary`: 3,732 raw, 3,133 retained and 599 excluded episode comments.
5. Recalculate overall like summary measures on **all source comments** rather than only on screened or selected records. Check zero-like records and any percentile or log transformation conventions before comparing results.

These checks use the supplied recorded fields. **The full historical data-collection and processing code, complete A–N matching rules, a comprehensive label-validation log and the engagement-proxy lexicon are not included in the archive.** Consequently, the package supports verification of stored data structures, screening tallies and descriptive calculations, together with qualitative inspection; it does **not** provide complete end-to-end computational replication of every original coding or collection step.

## 8. Ethical safeguards and responsible use

These files contain text from **publicly accessible social media**, not material solicited through participant recruitment. Before release, direct platform identifiers, screen names, profile links and identified contact details were removed or redacted; package-specific keys were assigned and timestamps were reduced to dates. These steps reduce risks but **do not guarantee anonymity**. Verbatim wording, context, rare expressions and within-dataset linkages may enable an outside reader to locate the original post or infer the author.

Please do not attempt to identify, contact or profile the original contributors. Avoid redistributing individual verbatim comments with additional identifiers, and assess privacy implications before secondary use. Public GitHub access does not, by itself, establish unrestricted copyright or privacy permissions for the underlying user-generated text. Reusers are responsible for their own ethics review, applicable law and platform terms.

If an individual record presents an unexpected identification or safety risk, contact the repository maintainer through GitHub to request a review. Changing files in a Git repository does not necessarily erase earlier versions from its commit history.

## 9. Scope and limitations

- Keyword/hashtag retrieval, platform visibility, deleted material and unavailable private interactions restrict coverage.
- The observation period starts on the first male approval date; it cannot establish pre/post causal change without a pre-approval comparison.
- The recorded labels overlap, some have incomplete lexicon documentation, and a substantial share of comments is unlabelled; these are not exhaustive or fully validated discourse-prevalence estimates.
- Screening partly depends on observed likes; the reported engagement figures are descriptive and apply to the unscreened source corpus.
- Missing complete reply-to relationships and date-only public records prevent precise reconstruction of conversational timing.
- The 20 episodes are purposively selected for interpretive contrast; user demographics, individual vaccination behavior and population-level attitudes cannot be inferred.
