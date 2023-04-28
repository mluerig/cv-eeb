---
layout: single
classes: wide
permalink: /speakers/ 
title: Invited keynote speakers

---

<div class="member-grid">

	{% for speaker in site.data.speaker_list %}

		<div itemscope.itemtype="https://schema.org/Person">
		
			<div class="member-content">

			<img src= " {{ speaker.avatar_path }}" alt="{{ speaker.name }}" >
			
			<h3> {{ speaker.name }} </h3>
			<p> {{ speaker.institute }} </p>

			<p> <a href="{{ speaker.website }}"> [website] </a> </p>
			
			<div class="member-bio" itemprop="description">
				<p> {{ speaker.bio }} </p>
			</div>
			
			</div>
		</div>
	
	{% endfor %}

</div>
