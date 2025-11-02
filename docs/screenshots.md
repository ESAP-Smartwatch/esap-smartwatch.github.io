---
layout: page
navname: Screenshots
title: Screenshots
description: Explore screenshots of the ESAP Smartwatch mobile app and hardware designs.
---

<link href="{{ site.baseurl }}/assets/micromodal.custom.css" rel="stylesheet">

{% assign imagenum = 0 %}

{% if imagenum == 0 %}
<div class="bg-gradient-to-br from-blue-50 to-purple-50 dark:from-gray-800 dark:to-gray-900 rounded-2xl p-12 text-center mb-8">
    <div class="text-6xl mb-4">📸</div>
    <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-3">Screenshots Coming Soon</h3>
    <p class="text-gray-600 dark:text-gray-400 mb-6">We're working on capturing beautiful screenshots of the ESAP Smartwatch app and hardware.</p>
    <p class="text-gray-500 dark:text-gray-500 text-sm">Add images to the <code class="bg-gray-200 dark:bg-gray-700 px-2 py-1 rounded">docs/screenshots/</code> folder to display them here.</p>
</div>
{% endif %}

<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
{% for image in site.static_files %}
{% if image.path contains 'screenshots/' %}
<div data-micromodal-trigger="{{ image.name }}" class="group cursor-pointer">
    <div class="relative overflow-hidden rounded-xl shadow-lg hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-1">
        <img class="object-cover w-full h-64 group-hover:scale-110 transition-transform duration-300" src="{{ site.baseurl }}{{ image.path }}" alt="Screenshot" />
        <div class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
    </div>
</div>
{% assign imagenum = imagenum | plus: 1 %}
{% endif %}
{% endfor %}
</div>

{% for image2 in site.static_files %}
{% if image2.path contains 'screenshots/' %}
<div class="modal micromodal-slide" id="{{ image2.name }}" aria-hidden="true">
<div class="modal__overlay" tabindex="-1" data-micromodal-close>
<img src="{{ site.baseurl }}{{ image2.path }}" style="max-width:90%;max-height:90vh;" alt="image"  role="dialog" aria-modal="true" aria-labelledby="{{ image2.name }}-title"/>
<div class="absolute top-0 right-0">
<button aria-label="Close modal" class="px-6 py-4 text-2xl text-gray-200" data-micromodal-close>&times;</button>
</div>
</div>
</div>
{% endif %}
{% endfor %}

<br>

<script src="https://unpkg.com/micromodal/dist/micromodal.min.js"></script>
<script src="{{ site.baseurl }}/assets/micromodal.custom.js"></script>
