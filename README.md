# Writing samples

I'm an experienced technical writer and author. My background spans decades in software, primarily as a developer, before transitioning into technical writing. This experience gives me the technical depth to understand and validate technical content, write clear, usable content for different audiences, write and test example code, and manage the documentation publishing toolchain. In addition to creating content, I've owned the information architecture, style, and editorial standards for sites that document rapidly evolving systems, and incorporated those standards into AI-assisted tooling that drafts and 
reviews documentation and ensures it stays up to date with product changes.

Co-author of Hadoop Application Architectures and Foundations for Architecting Data Solutions (O'Reilly Media) and technical editor and reviewer for several books on data processing and engineering. Previously co-founder and organizer of the Chicago Hadoop and Chicago Big Data user groups.

This page includes samples of my technical writing selected to demonstrate my ability to write clear, high-quality content across different documentation types and for different audiences.

## Grepr

### User guide: Integrating Grepr with external systems

Grepr acts as middleware between agents and observability platforms, so connecting to these systems and other services, such as cloud storage, is a core component of the Grepr platform. These connections are configured using Grepr integrations, so it's important that users can find complete, accurate, and usable documentation for their observability platforms and agents.

However, the existing documentation for this feature was captured on a single page that lacked conceptual information, examples of configuring connections for the user's vendor and agents, requirements and limitations for each connection type, and other important details. To address the documentation gaps and help users quickly find relevant content, I converted the single page into a new section in the site navigation. This section includes an index page providing an overview of Grepr integrations, and a separate page for each integration type, such as vendor and storage integrations. To guide users, the table of contents entries for this section and the section's pages use descriptive, intent-driven labels, titles, and headings.

The new section's index page, [Integrating Grepr with external systems](https://docs.grepr.ai/integrations/), provides a conceptual overview of integrations, guidance on using them, and links to dedicated pages for each supported integration.

To create cleaner, easier-to-consume content for the integrations pages, I used the Nextra Tabs component, allowing users to click a tab instead of scrolling past irrelevant information. To remove duplicate content across pages, I used a shared React component that accepts arguments for values and images that differ by integration type. The [Configure Datadog connections with a Grepr integration](https://docs.grepr.ai/integrations/datadog/) page provides an example of tab and component usage.

The initial content in this section was authored by me, with Claude used to validate details. Most subsequent updates, including changes to existing pages or the addition of a page for a new connection, were delegated to Claude.

### Conceptual/user guide: The Grepr storage layer

Storing raw data in a space-efficient, query-optimized format is a core component of the Grepr architecture. To provide this storage, Grepr uses a data lake deployed on Amazon S3, using widely-used open source formats. Although the data lake was referenced in the documentation, there was little detail on what data was stored, how it was stored, deployment options, and specific instructions for self-hosting. These gaps meant that team members spent time responding to customer requests for information and helping them deploy the required infrastructure when they chose to self-host the storage.

To fill these gaps and reduce the support burden, I created two pages:

- A conceptual page, [The Grepr data lake](https://docs.grepr.ai/grepr-platform/data-lake/),  with details on how the data lake is used, how it’s stored, and deployment options. This page was added to a new section containing conceptual documentation for the Grepr platform.
- A user guide, [Host a Grepr data lake with the Amazon S3 integration](https://docs.grepr.ai/integrations/aws-s3/), with details on configuring Grepr-hosted or self-hosted storage.

### Developer reference: The Grepr CLI

[The Grepr CLI](https://docs.grepr.ai/cli/) page is a complete guide to accessing Grepr functionality through the command line interface. This page documents the functionality provided by the CLI and all of its supported commands, but does not include details on command usage. Instead, the CLI help output is used as the authoritative documentation for running each command. Most of the page's content was drafted manually, with Claude used to generate comprehensive examples, validate technical content, and check it against the documentation site's standards.

### Conceptual/user guide: Trace pipelines in Grepr, drafted by Claude

The [Use a trace reduction pipeline for your APM data](https://docs.grepr.ai/pipelines/trace-pipelines/) page, which documents newly released trace pipeline functionality in Grepr, is an example of a first draft generated by Claude and edited by me. This is a relatively large page covering a lot of information, so using Claude allowed me to reduce several days of effort to about one day. The documentation was generated from the codebase using the style and other site standards that I defined and incorporated into the Claude instruction files.

I provided some guidance on the page's organization in the prompt, but left further organization and content decisions to Claude. These decisions included ensuring that the information is ordered so that the user always has the required context as they read through the page, as specified in Claude's instructions. The concise, readable explanation of APM data was also generated by Claude, based on instructions included in my prompt.

## Databricks

### User guide: Using watermarks for stateful processing

Processing large volumes of stateful streaming data with Spark, which is used by the Lakeflow pipelines framework, requires understanding how to use watermarks to manage state. The lack of detailed documentation for this feature led to customer support calls about pipeline failures. I wrote the [Optimize stateful processing with watermarks](https://docs.databricks.com/aws/en/ldp/stateful-processing) page to address this gap by detailing the recommended approach for processing streaming data with the Lakeflow pipelines framework on the Databricks platform. This page explains how to use watermarks and includes a range of examples for users to reference.

### Improving the usability of technical content

This is an example of how I've addressed “technical” doc debt. In other words, technical content that was vague, inaccurate, or incomplete. Specifically, I found that the content in the Autoreload for Python modules section on the [Work with Python and R modules](https://docs.databricks.com/aws/en/files/workspace-modules#autoreload-for-python-modules) page was vague and confusing. For example, it was unclear which cluster node types supported autoreload, and the explanation of the functionality was incomplete.

Although I didn't own this part of the documentation, I felt it was important to address these usability issues. To do this, I collaborated with the engineer who owned this feature to iterate on the changes required to create a more precise, understandable, and technically accurate description of the functionality.

### Tutorial example code: ETL with Lakeflow pipelines using public data and Python

Much of my original content from the [ETL with Lakeflow pipelines tutorial](https://docs.databricks.com/aws/en/getting-started/data-pipeline-get-started) has been updated by other writers as the product has evolved. I'm including this page because it retains the original example I created for the tutorial, including the example data set used, my Python and SQL code, and the steps required to complete it.

### Blog post: The importance of metadata

[Metadata > Data](https://medium.com/97-things/metadata-data-2703342e9434) is a short post on the importance of metadata, written at the request of O'Reilly for inclusion in [97 Things Every Data Engineer Should Know](https://www.oreilly.com/library/view/97-things-every/9781492062400/).

## Resume

- https://www.linkedin.com/in/jaseidman/
- [Download my resume](/files/JonathanSeidman-Resume-TechWriter.pdf)
