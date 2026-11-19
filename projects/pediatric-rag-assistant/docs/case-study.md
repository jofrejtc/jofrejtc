# Pediatric RAG assistant case study

## Context and objective

I built this project for the Technological Trends course at La Salle Campus Barcelona in April 2026. The use case was an informational assistant for first-time parents. The engineering objective was to connect a scoped knowledge base to a conversational interface, test its behaviour and document the effect of prompt changes.

The prototype was configured through Capacity Console. Its retrieval, indexing and model infrastructure are managed by the platform.

## Knowledge-base design

I organised the uploaded material into topic folders and text-oriented files. Topics included fever, respiratory symptoms, hydration, feeding, newborn care, sleep and warning signs.

This organisation was intended to help retrieval find relevant passages and reduce ambiguity between unrelated topics. I configured folder access for the dedicated project concierge.

The public documentation records the taxonomy. Exact source URLs, full document versions and the underlying corpus require a separate provenance record before a reproducible or clinically reviewed deployment.

## Conversation design

The main entry point was a guided fever exchange with Spanish inquiry variants. An AI Agent Card inside the exchange used retrieved knowledge-base content to compose the answer.

The prompt defined the informational role, the retrieved-source requirement and the desired calm, concise language. A screenshot of that configuration is included in the project.

The guided layer controlled which inputs reached the agent. This made inquiry coverage a practical constraint. The report records that a broad message such as “Mi bebé no está bien” needed a suitable configured route.

## Implementation and web integration

I created a dedicated Web Concierge and copied the embed configuration into a local HTML page. The public integration template contains an empty concierge token, allowing another builder to connect their own concierge.

The original website screenshot and platform settings informed the write-up. Public evidence was selected from the academic report to show the work without exposing the classroom account directory or the original widget identifiers.

## Testing and observations

I tested fever questions, a vomiting and reduced-drinking scenario and an outside-scope question about a dog. The recorded dog query received an insufficient-information response.

I also compared responses to a fever question while changing the prompt. The report describes improved concision and earlier follow-up questions. The available screenshots are partial and the before-and-after placement is ambiguous, so the public evaluation treats the result as qualitative.

Clinical correctness, retrieval precision, latency and overall accuracy remain unevaluated. A controlled next iteration would record complete transcripts, prompt versions, retrieved sources and clearly defined evaluation criteria.

## Conclusions and next iteration

The project gave me practical experience with knowledge-base organisation, access configuration, guided conversations, prompt refinement and evidence-based technical documentation.

The main design finding was that retrieval content and conversation routing both influence usefulness. A well-organised knowledge base still needs entry points that cover the questions people ask.

Proposed improvements include broader inquiry coverage, a carefully evaluated fallback, topic and age metadata, source versioning, and a documented route to human review.

## Evidence origin

This case study is adapted from my final academic report, updated on 12 April 2026. The original sections “Prompt refinement comparison” and “Conclusion” contain the qualitative comparison and closing reflections. Screenshots in this repository are selected original captures from that report.
