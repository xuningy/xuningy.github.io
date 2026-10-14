---
layout: default
---

<img class="profile-picture" src="{{site.baseurl}}/{{site.profile-picture}}">

I am a Senior Research Scientist at the [Seattle Research Lab (SRL)](https://research.nvidia.com/labs/srl/) at NVIDIA, working on robotics and AI. My research interests include generalist robot policies, evaluation and benchmarking. I received my Ph.D. in Robotics from Carnegie Mellon University, and my B.A.Sc. in Engineering Science from the University of Toronto, with a major in Aerospace.

You can contact me at xuningy at nvidia dot com.

### Highlights

- <span class="highlight-date">10/2026</span> Released [Astranomy](https://research.nvidia.com/labs/srl/projects/astranomy/), an empirical study of GPT-6 Astra as a native robot policy
- <span class="highlight-date">10/2026</span> Released [ARC](https://arc-robot-reasoning.github.io/), a reasoning recipe for robot foundation models
- <span class="highlight-date">09/2026</span> [VoLo](https://chicychen.github.io/VoLo/) has been accepted to CoRL 2026 (33% AR)!
- <span class="highlight-date">08/2026</span> Released [DROID+](https://github.com/nvlabs/droidplus), a simplified hardware control stack for the DROID robot platform
- <span class="highlight-date">07/2026</span> Gave two invited talks: [Australian Centre for Robotics](https://robotics.sydney.edu.au/) at the University of Sydney and [University of New South Wales](https://www.unsw.edu.au/)
- <span class="highlight-date">07/2026</span> Gave a talk at the RSS 2026 workshop [Toward Open-World Failure Recovery for Robots](https://csiro-robotics.github.io/failure-recovery/)
- <span class="highlight-date">07/2026</span> Invited panelist at the RSS 2026 workshop [Trustworthy Embodied Foundation Models](https://robot-fm-safety.github.io/index.html)
- <span class="highlight-date">07/2026</span> Wrote a [blog](https://developer.nvidia.com/blog/how-to-evaluate-general-purpose-robot-policies-for-real-world-deployment/) on how to evaluate general-purpose robot policies for real-world deployment
- <span class="highlight-date">04/2026</span> [RoboLab](https://research.nvidia.com/labs/srl/projects/robolab/) has been accepted to RSS 2026 (29.7% AR)!
- <span class="highlight-date">04/2026</span> [AdaVoMP](https://research.nvidia.com/labs/sil/projects/adavomp/) has been accepted to ICML 2026 (26.6% AR)!

<details class="more-highlights" markdown="1">
<summary><span class="more-label">More highlights</span><span class="less-label">Fewer highlights</span></summary>

- <span class="highlight-date">04/2026</span> [RoboLab](https://research.nvidia.com/labs/srl/projects/robolab/) is released! Highlighted in Nvidia's [National Robotics Week](https://blogs.nvidia.com/blog/national-robotics-week-2026/)
- <span class="highlight-date">05/2024</span> Built an automatic [pick-and-place pipeline in simulation](https://blogs.nvidia.com/blog/national-robotics-week-2026/) in collaboration with Intrinsic.AI: [TechCrunch](https://techcrunch.com/2024/05/06/alphabet-owned-intrinsic-incorporates-nvidia-tech-into-robotics-platform/), [AI Business](https://aibusiness.com/verticals/nvidia-intrinsic-collaborate-to-enhance-robot-task-management), [The Robot Report](https://www.therobotreport.com/intrinsic-uses-nvidia-foundation-model-to-improve-robotic-grasping/)
- <span class="highlight-date">2019</span> In-place hover-to-hover flip of a quadrotor, featured by [Rapyuta Robotics](https://www.youtube.com/watch?v=zqp2Z2hbOFU-)

</details>

### Selected publications

{% assign selected = site.data.papers | where: "selected", true %}
<div class="pub-list">
{% for p in selected %}{% include paper.html paper=p %}{% endfor %}
</div>

<p class="pub-more"><a href="{{ site.baseurl }}/papers">View all publications →</a></p>

<hr>

### Some Old Robots
<div class="rowofposts">

{% for post in site.posts %}
  {% if post.category == "robot" %}

      {% include postbox-nosnippet.html %}
      {% endif %}
    {% endfor %}

</div>
