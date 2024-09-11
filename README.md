# Let's see the current and the future of the Linux with LLM Agent

Imagine if you can ask every kernel developer to do a completed survey/questionare about a commit/a mail, what can you find with the results? Researcher has proved that LLM can acheive similar level as human when doing summary/survey/questionare task in Market, Chemistry... Such system is also deployed and explored in production for... (See the citation)

Workflow/Method: 

```
[Human Experts (LLM) design survey] -> [LLM Agent complete survey] -> [Human Experts (LLM) evaluate survey results samples] -> [Human Experts (LLM) give the report]
```

Let's take eBPF as an example, the same tool can be directly applied to other subsystems.

## Datasets with eBPF: Linux BPF subsystem

- 680+ eBPF expert seleted Important feature commits information, with feature name, type(Map, helper, kfunc, prog, attach, etc...)
- bpf related feature commits information, with LLM Agent survey and summary
- 120000+ All bpf subsystem related mails, with LLM Agent survey
- vector index for all of them

All the datasets are automatically updated by CI! The interative analysis is on the way to deployment...

## Analysis and insights

Based on the contents of the CSV, which include data on commit IDs, feature types, feature names, authors, commit messages, and dates, here are some insightful questions that could lead to further exploration or research:

1. **Feature Development Trends**:

   - What are the most frequently introduced feature types in the eBPF kernel codebase? 
   - How has the introduction of various program types (e.g., `BPF_PROG_TYPE_SOCKET_FILTER`, `BPF_PROG_TYPE_KPROBE`) evolved over time?

2. **Impact of Key Contributors**:

   - How much of the eBPF feature development is driven by key contributors like Alexei Starovoitov and Daniel Borkmann?
   - Are there particular features or components of eBPF that specific contributors tend to focus on?

3. **Commit Frequency and Changes**:
   - Are there periods of rapid feature introduction or major changes in eBPF development (indicated by commit frequency)?
   - Which feature types tend to have the most revisions, based on the number of related commits?

4. **Commit Patterns**:
   - Are there any patterns in commit messages that indicate specific challenges or areas of focus (e.g., performance improvements, bug fixes, or new feature introductions)?
   - What types of program types are often accompanied by significant commit messages indicating large functional changes?

5. **Reviewer/Committer Influence**:
   - How significant is the role of specific committers (e.g., David S. Miller, Ingo Molnar) in shaping the direction of eBPF development?
   - Are certain features or feature types often reviewed by specific individuals?

6. **Feature Maturity**:
   - Which features have the most development and refinement (e.g., multiple commits over time), indicating a longer process toward maturity?
   - Are newer features in eBPF, like tracepoint integration (`BPF_PROG_TYPE_TRACEPOINT`), being actively developed, and how do their commit histories compare to older features?

These questions can help guide a deeper analysis of the kernel eBPF feature development process, as well as the key players involved in it.

## Graphs to have

The dataset contains information about BPF features, including commit details such as the author, commit message, date, feature type, and feature name. Based on this data, here are some interesting graph ideas to gain insights:

Timeline of Feature Introductions:

- Plot a timeline that shows when different BPF features (grouped by feature_type or feature_name) were introduced. This can reveal trends in the development of certain BPF features over time.

Commits by Author:


- A bar chart or pie chart showing the number of commits per author. This can highlight key contributors to the BPF feature set.
Feature Type Distribution:
- A pie chart or bar chart to visualize the distribution of commits across different feature_type. This can provide insights into which types of BPF features received more development focus.

Feature Introduction over Time by Type:

- A stacked area chart showing how different feature_type were introduced over time. This can help understand the evolution of different BPF program types or functionalities.

Top Features by Commit Activity:

A bar chart that shows which features (feature_name) have the most commits associated with them. This can identify the most actively developed BPF features.
