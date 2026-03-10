---
name: indian-constitution
description: AI-powered legal assistant for Indian Constitution and BNS (Bharatiya Nyaya Sanhita, replaced IPC). Query constitutional provisions and criminal law sections using RAG with semantic search.
compatibility: Created for Zo Computer
metadata:
  author: buckbuckbot.zo.computer
  category: legal
  tags: constitution, india, law, legal, bns, ipc, lawyer, rag

---

# Indian Constitution + BNS Lawyer Skill

Complete RAG-based legal assistant for Indian constitutional law and criminal law (BNS 2023).

## What You Can Ask

### Constitutional Law
- "What are fundamental rights under Part III?"
- "How is the President elected?"
- "What are directive principles?"
- "Emergency provisions in Constitution"
- "Article 370 and special status"

### BNS 2023 (Replaced IPC)
- "What is punishment for murder under Section 103 BNS?"
- "Hate speech laws in BNS"
- "Sedition under Section 150 BNS"
- "Domestic violence sections in BNS"
- "Section 299 BNS - hate speech"

## Quick Start

```bash
# Query Constitution
python3 scripts/query.py "What are fundamental rights?"

# Query BNS
python3 scripts/query.py "What is Section 103 BNS?"

# Get more results
python3 scripts/query.py "Emergency provisions" -k 10
```

## Constitutional Hierarchy

### Parts of the Constitution
1. **Part I**: The Union and its Territory (Articles 1-4)
2. **Part II**: Citizenship (Articles 5-11)
3. **Part III**: Fundamental Rights (Articles 12-35)
4. **Part IV**: Directive Principles of State Policy (Articles 36-51)
5. **Part IVA**: Fundamental Duties (Article 51A)
6. **Part V**: The Union (Articles 52-151)
7. **Part VI**: The States (Articles 152-237)
8. **Part VII**: The States in Part B of First Schedule (Repealed)
9. **Part VIII**: The Union Territories (Articles 239-242)
10. **Part IX**: The Panchayats (Articles 243-243O)
11. **Part IXA**: The Municipalities (Articles 243P-243ZG)
12. **Part IXB**: The Co-operative Societies (Articles 243ZH-243ZT)
13. **Part X**: The Scheduled and Tribal Areas (Articles 244-244A)
14. **Part XI**: Relations between the Union and the States (Articles 245-263)
15. **Part XII**: Finance, Property, Contracts and Suits (Articles 264-300A)
16. **Part XIII**: Trade, Commerce and Intercourse (Articles 301-307)
17. **Part XIV**: Services under the Union and the States (Articles 308-323)
18. **Part XIVA**: Tribunals (Articles 323A-323B)
19. **Part XV**: Elections (Articles 324-329A)
20. **Part XVI**: Special Provisions (Articles 330-342)
21. **Part XVII**: Official Language (Articles 343-351)
22. **Part XVIII**: Emergency Provisions (Articles 352-360)
23. **Part XIX**: Miscellaneous (Articles 361-367)
24. **Part XX**: Amendment of the Constitution (Article 368)
25. **Part XXI**: Temporary, Transitional and Special Provisions (Articles 369-392)
26. **Part XXII**: Short Title, Commencement, Authoritative Text (Articles 393-395)

### Important Schedules
- **First Schedule**: Names of States and UTs
- **Second Schedule**: Salaries and allowances
- **Third Schedule**: Forms of Oaths
- **Fourth Schedule**: Allocation of seats in Rajya Sabha
- **Fifth Schedule**: Provisions for Scheduled Areas
- **Sixth Schedule**: Provisions for Tribal Areas
- **Seventh Schedule**: Union, State, Concurrent Lists
- **Eighth Schedule**: Official Languages (22 languages)
- **Ninth Schedule**: Laws protected from judicial review
- **Tenth Schedule**: Anti-defection provisions
- **Eleventh Schedule**: Panchayat powers
- **Twelfth Schedule**: Municipality powers

## BNS 2023 (Bharatiya Nyaya Sanhita)

### What is BNS?
The **Bharatiya Nyaya Sanhita, 2023** (BNS) replaced the **Indian Penal Code, 1860 (IPC)** from **July 1, 2024**. It modernizes India's criminal law with:
- Reduced sections (358 vs 511 in IPC)
- Gender-neutral provisions
- New offences (community service, organized crime)
- Enhanced punishments for crimes against women

### Key BNS Sections

| Section | Offence | Punishment |
|---------|---------|------------|
| **103** | Murder | Death or life imprisonment + fine |
| **105** | Culpable homicide | Life imprisonment or 10 years + fine |
| **150** | Sedition | 7 years to life imprisonment |
| **196** | Promoting enmity (hate speech) | 3 years imprisonment |
| **197** | Imputations prejudicial to integration | 3 years imprisonment |
| **299** | Deliberate acts intended to outrage religious feelings | 3 years imprisonment |
| **100** | Snatching | 3 years imprisonment + fine |
| **304** | Mob lynching | Death, life imprisonment, or 7 years |
| **352** | Assault or criminal force to woman | 1-5 years imprisonment |
| **69** | Sexual intercourse by employing deceitful means | 10 years imprisonment |

### Major Changes from IPC
- **Sedition (124A IPC)** → **Section 150 BNS** (narrowed scope)
- **Section 377 IPC** (unnatural offences) → **Deleted** (decriminalized)
- **Section 309 IPC** (attempt to suicide) → **Decriminalized** (now Section 226 with focus on rehabilitation)
- **New Section 69**: Sexual intercourse by deceitful means
- **New Section 304**: Mob lynching as separate offence
- **Community Service**: For petty offences (6 new provisions)

### Data Coverage
| Document | Details |
|----------|---------|
| **Constitution of India** | 402 pages, 395 Articles |
| **BNS 2023** | 102 pages, 358 Sections |
| **Total Corpus** | 1.27M characters, 2,265 chunks |
| **Effective Date** | July 1, 2024 |

## Data Source

- **Document**: Constitution of India (as of July 2024)
- **Source**: https://cdnbbsr.s3waas.gov.in/
- **Pages**: 402
- **Chunks**: 1,726
- **Embedding Model**: all-MiniLM-L6-v2 (384 dimensions)
- **Vector Store**: ChromaDB
- **Chunk Size**: 1000 characters with 200 overlap

## Important Notes

1. **Not Legal Advice**: This skill provides constitutional information but is NOT a substitute for professional legal counsel.

2. **Updated as of 2024**: Contains amendments up to the 106th Constitutional Amendment Act, 2023.

3. **Citations**: All responses include relevant Article numbers for verification.

4. **Interpretation**: Constitutional interpretation varies; consult Supreme Court judgments for authoritative interpretation.

## Use Cases

### For Citizens
- Know your fundamental rights
- Understand voting procedures
- Learn about legal protections

### For Law Students
- Quick constitutional research
- Article cross-referencing
- Amendment tracking

### For Lawyers
- Draft legal arguments
- Find constitutional provisions
- Verify citations

### For UPSC/PSC Aspirants
- Constitutional studies
- Quick revision
- Article memorization

## Technical Details

### Embedding Model
- **Model**: all-MiniLM-L6-v2
- **Size**: ~80MB (much smaller than Gemma-300M)
- **Dimensions**: 384
- **Speed**: Fast CPU inference
- **Accuracy**: High quality for semantic search

### Retrieval Settings
- **Top-k**: 5 chunks per query
- **Similarity**: Cosine similarity
- **Chunk overlap**: 200 characters (for context continuity)

## Future Enhancements

- [ ] Add Supreme Court judgments
- [ ] Add legal commentary
- [ ] Add bare acts integration
- [ ] Add amendment history
- [ ] Add comparative constitutional law

---

**We the People of India** 🇮🇳  
*Created: March 2026*  
*Constitution Version: As of July 2024*
