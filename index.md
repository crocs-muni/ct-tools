---
---

<h1 style="display: flex; align-items: center; color: black; font-weight: bold;"><img src="{{ "/assets/img/logo.svg" | relative_url }}" /><span style="margin-left: 1em;">Constant-timeness verification tools</span></h1>


This page lists tools for testing and verification of constant-timeness of programs.
The table is based mostly on the work in [*“They’re not that hard to mitigate”: What Cryptographic Library Developers Think About Timing Attacks*](https://crocs.fi.muni.cz/public/papers/usablect_sp22) and
[*“These results must be false”: A usability evaluation of constant-time analysis tools*](https://crocs.fi.muni.cz/public/papers/usablect_usenix24) with addition of more tools. 
Each tool has its own page with more information and resources, sometimes **even a tutorial on using the tool**.

There are currently {{ site.tools.size }} tools in the table.

## Tools

<table id="tool-table">
<thead>
	<th onclick="sortTableString('tool-table', 0)" title="Click to sort" class="pointer">Name</th>
	<th onclick="sortTableYear('tool-table', 1)"   title="Click to sort" class="pointer">Year</th>
	<th onclick="sortTableString('tool-table', 2)" title="Click to sort" class="pointer">Target</th>
	<th onclick="sortTableString('tool-table', 3)" title="Click to sort" class="pointer">Technique</th>
	<th onclick="sortTableString('tool-table', 4)" title="Click to sort" class="pointer">Guarantees</th>
	<th onclick="sortTableString('tool-table', 5)" title="Click to sort" class="pointer">Tutorial</th>
</thead>
{% assign tools = site.tools | sort_natural: "title" %}
{% for tool in tools %}
	{% assign tutorials = site.tutorials | where: "title", tool.title %}
	<tr>
		<td><a href="{{ tool.url | relative_url }}">{{ tool.title }}</a></td>
		<td>{{ tool.year }}</td>
		<td>{{ tool.target }}</td>
		<td>{{ tool.technique }}</td>
		<td>{{ tool.guarantees }}</td>
		<td>{% if tutorials and tutorials.size > 0 %}<a href="{{ tutorials[0].url | relative_url }}">yes</a>{% endif %}</td>
	</tr>
{% endfor %}
</table>

Note that the claims w.r.t. guarantees in this table are **best effort** and may be wrong.
Many tools do not claim any guarantees about their analysis.

## Examples

The following list constains short snippets of C code that exhibit constant-time (or not) behavior and
can be useful for testing constant-timeness verification tools, or learning how to use them.

{% assign examples = site.examples | sort_natural: "title" %}
<ul>
{% for example in examples %}
	<li><a href="{{ example.url | relative_url }}">{{ example.title }}.c</a> ({% if example.ct == "depends" %}depends{% elsif example.ct %}CT{% else %}non-CT{% endif %})</li>
{% endfor %}
</ul>

## Resources

The resources below can be helpful if you are seeking more information on these tools or constant-time code in general.

- [Blog: The state of tooling for verifying constant-timeness of cryptographic implementations](https://neuromancer.sk/article/26) <br/>
  Constitutes a precursor to this site, some reasoning for the classification used on this site is given there.
- [“They’re not that hard to mitigate”: What Cryptographic Library Developers Think About Timing Attacks](https://crocs.fi.muni.cz/public/papers/usablect_sp22) <br/>
  Presents a survey done among cryptographic library developers into their view on timing attacks,
  their mitigation and constant-timeness analysis tools.
- [“These results must be false”: A usability evaluation of constant-time analysis tools](https://crocs.fi.muni.cz/public/papers/usablect_usenix24) <br/>
  Presents a user study evaluating the usability of some constant-timeness analysis tools: Binsec, ct-verif, dudect, valgrind, MemSan, haybale-pitchfork.
- [A Systematic Evaluation of Automated Tools for Side-Channel Vulnerabilities Detection in Cryptographic Libraries](https://arxiv.org/pdf/2310.08153) <br/>
  Presents a thorough and systematic classification of 34 constant-timeness analysis tools.
- [Blog: Testing constant-timeness using Valgrind: case of the NSS library](https://neuromancer.sk/article/29) <br/>
  Case study on using Valgrind for constant-timeness analysis of the NSS library.
- [Blog: Constant-time code verification with Memory Sanitizer](https://www.amongbytes.com/posts/20210709-testing-constant-time/20210709-testing-constant-time.html) <br/>
  Case study on using MemSan for constant-timeness analysis.

## Miscellaneous

The articles below mostly discuss the role of compilers in introducing (and potentially mitigating) timing leaks.

- [What you get is what you C: Controlling side effects in mainstream C compilers](https://www.cl.cam.ac.uk/archive/rja14/Papers/whatyouc.pdf)
- [Breaking Bad: How Compilers Break Constant-Time Implementations](https://arxiv.org/pdf/2410.13489)
- [Clang vs. Clang: You're making Clang angry. You wouldn't like Clang when it's angry.](https://blog.cr.yp.to/20240803-clang.html)
- [Architectural Mimicry: Innovative Instructions to Efficiently Address Control-Flow Leakage in Data-Oblivious Programs](https://mici.hu/papers/winderix24ami.pdf)
 
<hr/>
<img src="assets/img/oprah.jpg" alt="Oprah giving everyone a tool" style="display: block; margin-left: auto; margin-right: auto;"/>
