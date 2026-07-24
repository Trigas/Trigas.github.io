---
title: "About"
layout: homelay
description: "Pedro Trigueira — Senior Delivery Architect at Cisco CX EMEA. Cloud-native security, AI infrastructure, eBPF."
permalink: /
---

<div class="ascii-art glow-pulse" aria-hidden="true">
██████╗ ███████╗██████╗ ██████╗  ██████╗
██╔══██╗██╔════╝██╔══██╗██╔══██╗██╔═══██╗
██████╔╝█████╗  ██║  ██║██████╔╝██║   ██║
██╔═══╝ ██╔══╝  ██║  ██║██╔══██╗██║   ██║
██║     ███████╗██████╔╝██║  ██║╚██████╔╝
╚═╝     ╚══════╝╚═════╝ ╚═╝  ╚═╝ ╚═════╝
████████╗██████╗ ██╗ ██████╗ ██╗   ██╗███████╗██╗██████╗  █████╗
╚══██╔══╝██╔══██╗██║██╔════╝ ██║   ██║██╔════╝██║██╔══██╗██╔══██╗
   ██║   ██████╔╝██║██║  ███╗██║   ██║█████╗  ██║██████╔╝███████║
   ██║   ██╔══██╗██║██║   ██║██║   ██║██╔══╝  ██║██╔══██╗██╔══██║
   ██║   ██║  ██║██║╚██████╔╝╚██████╔╝███████╗██║██║  ██║██║  ██║
   ╚═╝   ╚═╝  ╚═╝╚═╝ ╚═════╝  ╚═════╝ ╚══════╝╚═╝╚═╝  ╚═╝╚═╝  ╚═╝
</div>

<!-- ═══════════ ABOUT TAB ═══════════ -->
<div class="content-tab-panel active" id="tab-about">

<div class="section-prompt">
<span class="dollar">$</span> <span class="cmd">whoami</span>
</div>

<div class="cmd-output stagger-children">
{% for member in site.data.pi %}
<p><span class="output-line" style="color: var(--text-primary); font-weight: 600; font-size: 1.2rem;">{{ member.name }}</span>
<span class="output-line" style="color: var(--amber);">{{ member.info }}</span>
</p>

<div style="display: flex; align-items: flex-start; gap: 1.5rem; flex-wrap: wrap; margin: 1rem 0;">
<img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" alt="{{ member.name }}" style="width: 130px; height: 130px; border-radius: 50%; border: 2px solid var(--green); object-fit: cover;">
<div style="font-size: 0.95rem; line-height: 1.8;">
<span style="color: var(--text-muted);">📧</span> <a href="mailto:{{ member.email }}">{{ member.email }}</a><br>
<span style="color: var(--text-muted);">🐙</span> <a href="{{ member.github }}" target="_blank">GitHub</a><br>
<span style="color: var(--text-muted);">💼</span> <a href="{{ member.linkedin }}" target="_blank">LinkedIn</a>
</div>
</div>
{% endfor %}
</div>

<div class="section-prompt">
<span class="dollar">$</span> <span class="cmd">tree ~/career</span>
</div>

{% for member in site.data.pi %}
<div class="tree stagger-children">
{% for educ in (1..member.number_educ) %}
{% assign start_key = "education" | append: educ | append: "_start" %}
{% assign end_key = "education" | append: educ | append: "_end" %}
{% assign detail_key = "education" | append: educ | append: "_detail" %}
<div class="tree-item">
{% assign short_key = "education" | append: educ | append: "short" %}
<span class="tree-date" {% if member[start_key] %}data-start="{{ member[start_key] }}"{% endif %} {% if member[end_key] %}data-end="{{ member[end_key] }}"{% endif %}>{{ member[short_key] }}</span>
<span class="tree-label">{% if member[detail_key] %}<br><span style="color: var(--text-muted); font-size: 0.9rem;">{{ member[detail_key] }}</span>{% endif %}</span>
</div>
{% endfor %}
</div>
{% endfor %}

<div class="section-prompt" style="margin-top: 2rem;">
<span class="dollar">$</span> <span class="cmd">cat about.md</span>
</div>

<div class="about-text" style="color: var(--text-secondary); line-height: 1.8; max-width: 75ch;">

Technology is accelerating faster than our ability to adapt. My focus is on building resilient Service Provider networks and datacenter architectures that anticipate disruption — spanning cloud-native security, AI infrastructure, and secure multi-site designs for the exponential age.

Over 20 years in the SP telecom industry across multiple countries and regions. Now driving **Isovalent/Cilium and eBPF-based runtime security** adoption alongside **AI infrastructure delivery** and datacenter migrations. Author of the patent-pending **AICDN** concept applying CDN architecture principles to AI inference cost reduction.

</div>

</div>

<!-- ═══════════ NEWS TAB ═══════════ -->
<div class="content-tab-panel" id="tab-news">

<div class="section-prompt">
<span class="dollar">$</span> <span class="cmd">tail -10 ~/news.log</span>
</div>

<div class="stagger-children">
{% for article in site.data.news limit:10 %}
<div class="news-item" style="margin-bottom: 1.5rem; padding-left: 1rem; border-left: 2px solid var(--border);">
<span style="color: var(--amber); font-size: 0.85rem;">{{ article.date }}</span>
<p style="margin: 0.25rem 0 0;">{{ article.headline }}</p>
</div>
{% endfor %}
</div>

</div>

<!-- ═══════════ PERSONAL/INTERESTS TAB ═══════════ -->
<div class="content-tab-panel" id="tab-personal">

<div class="section-prompt">
<span class="dollar">$</span> <span class="cmd">cat ~/interests.md</span>
</div>

<div style="color: var(--text-secondary); line-height: 1.8; margin-bottom: 2rem;">

🚴 Road &amp; MTB cycling; marathon running<br>
⚽ Football (Sporting CP supporter)<br>
🏄 Surfing; snowboarding<br>
🇵🇹 Based in Lisbon, Portugal

</div>

<div class="section-prompt" style="margin-top: 2rem;">
<span class="dollar">$</span> <span class="cmd">cat /etc/skills | head -20</span>
</div>

<div style="color: var(--text-secondary); line-height: 1.8;">

<code>Cloud-native Security</code> · <code>Cilium CNI</code> · <code>Tetragon</code> · <code>eBPF</code> · <code>Hubble</code><br>
<code>Datacenter</code> · <code>VXLAN-EVPN</code> · <code>Nexus 9000</code> · <code>ACI</code> · <code>vPC</code><br>
<code>AI Infrastructure</code> · <code>GPU Clusters</code> · <code>RoCEv2</code> · <code>NVLink</code> · <code>VAST Data</code><br>
<code>Mobile Packet Core</code> · <code>3GPP</code> · <code>EPC/5GC</code> · <code>ASR5000</code><br>
<code>Kubernetes</code> · <code>OpenShift</code> · <code>k3s</code> · <code>Helm</code> · <code>Lima</code><br>
<code>Python</code> · <code>Ansible</code> · <code>Automation</code> · <code>Jekyll</code> · <code>GitHub Pages</code>

</div>

</div>
