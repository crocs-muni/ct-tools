---
---
## Constant-timeness verification tools

This page lists tools for testing and verification of constant-timeness of programs.
The table is based mostly on the work in [*“They’re not that hard to mitigate”: What Cryptographic Library Developers Think About Timing Attacks*](https://crocs.fi.muni.cz/public/papers/usablect_sp22) with addition of more tools. 
Each tool has its own page with more information and resources, sometimes **even a tutorial on using the tool**.

There are currently {{ site.tools.size }} tools in the table.

## Tools

<table>
<thead>
	<th>Name</th>
	<th>Year</th>
	<th>Target</th>
	<th>Technique</th>
	<th>Guarantees</th>
	<th>Tutorial</th>
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

- <https://neuromancer.sk/article/26>
- <https://crocs.fi.muni.cz/public/papers/usablect_sp22>
- <https://neuromancer.sk/article/29>

<hr/>
<img src="assets/img/oprah.jpg" alt="Oprah giving everyone a tool" style="display: block; margin-left: auto; margin-right: auto;"/>
