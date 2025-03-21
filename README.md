# Mithril Search Engine

## About

Mithril is a distributed web search engine built from scratc by students at the University of Michigan. This is our [EECS 498 System Design of Search Engine](https://web.eecs.umich.edu/~nham/eecs440w21/) capstone project under Professor Nicole Hamilton.

## What is our crawler doing?

If you've seen our crawler hitting your site, we're collecting web pages for academic research purposes. Our crawler:

- Respects robots.txt directives
- Uses exponential backoff for rate limiting
- Identifies itself with a clear user-agent
- Maintains a reasonable request rate per domain

We're not scraping for commercial purposes or training an LLM - just building a search engine for a class project.

## The Team

We're "The Fellowship of the Ring Buffer" - seven senior/sophomore CS and Math students interested in distributed systems, performance optimization, and systems programming.

## Technical Details

Our engine consists of several components:

- **Crawler**: Multi-threaded with connection pooling and adaptive rate limiting
- **Index**: SPIMI-based inverted index with variable-byte encoding and position data
- **Query Engine**: Boolean and phrase queries with optimized constraint solving
- **Ranking**: [In development]

The entire system is written in C++ with a focus on performance. Our inverted index uses memory-mapped files, aggressive compression, and our own custom data structures.

## Contact

If you have concerns about our crawler, please contact:
- mithril498@umich.edu

---

*Built by the "Fellowship of the Ring Buffer" at the University of Michigan, 2025*
