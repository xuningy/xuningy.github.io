---
layout: default
---

<img class="profile-picture" src="{{site.baseurl}}/{{site.profile-picture}}">

I received my Ph.D. from the [Robotics Institute](https://www.ri.cmu.edu/), Carnegie Mellon University in Jan 2022. I obtained my B.A.Sc. in [Engineering Science](https://engsci.utoronto.ca/program/what-is-engsci/) with Honours from University of Toronto, with a major in [Aerospace Engineering](http://www.utias.utoronto.ca/) and a minor in Robotics and Mechatronics.

My work focuses on human intention modeling and prediction for continuous human-in-the-loop control of mobile robots, and agile safe navigation in unknown and unstructured environments. My areas of interest include motion planning, dynamics and control, human robot interaction (HRI), human intention modeling, and bayesian inference for human decision making.

You can contact me at xuningy at gmail dot com. I am actively seeking opportunities.

### Thesis
1. **Human-in-the-loop Planning for Mobile Robots**  
*PhD Thesis, Robotics Institute, Carnegie Mellon University, Jan 2022*   
\[[document to come]()\]
\[[talk](https://youtu.be/0qSzzafpmxo)\]


### Publications

1. [**An Intention Guided Hierarchical Framework for Trajectory-based Teleoperation of Mobile Robots**](/papers/icra21.pdf)  
 **Xuning Yang**, Jasmine Cheng, and Nathan Michael  
*International Conference on Robotics and Automation (ICRA), 2021*  
\[[bibtex](bibtex/icra21.txt)\]
\[[code](https://github.com/xuningy/planning_arch)\]
\[[talk](https://youtu.be/XNVsO4b2sw4)\]
[<a class="gif-link" id="icra21">gif</a>]
<img class="gif" id="icra21-gif" src="assets/gifs/icra21.gif"/>

2. [**An imminent collision monitoring system with safe stopping
interventions for autonomous aerial flights**](/papers/icra21-ws.pdf)  
Jasmine Cheng,  **Xuning Yang**, and Nathan Michael  
*ICRA 2021 Workshop on "Resilient and Long-Term Autonomy for Aerial Robotic Systems", Spotlight Talk*  
\[[bibtex](bibtex/icra21-ws.txt)\]
<!-- \[[video](https://youtu.be/Tulya5WtB_Y)\] -->

3. [**Assisted Mobile Robot Teleoperation with Intent-aligned Trajectories via Biased Incremental Action Sampling**](/papers/IROS20.pdf)  
 **Xuning Yang** and Nathan Michael  
*International Conference on Intelligent Robots and Systems (IROS), October 2020*  
\[[bibtex](bibtex/iros20.txt)\] \[[code](https://github.com/xuningy/motion_primitive_tree)\]
\[[talk](https://youtu.be/Tulya5WtB_Y)\]
[<a class="gif-link" id="iros20">gif</a>]
<img class="gif" id="iros20-gif" src="assets/gifs/iros20.gif"/>

4. [**Fast and Agile Vision-Based Flight with Teleoperation and Collision Avoidance on a Multirotor**](/papers/ISER18.pdf)  
Alexander Spitzer\*, **Xuning Yang\***, John Yao, Aditya Dhawale, Kshitij Goel, Mosam Dabhi, Matt Collins, Curtis Boirum, and Nathan Michael  
*International Symposium on Experimental Robotics (ISER), November 2018*  
\[[bibtex](bibtex/iser18.txt)\]  \[[video](https://www.youtube.com/watch?v=_-KmGhP0HTQ)\]
[<a class="gif-link" id="vibworld">sim</a>/<a class="gif-link" id="hsv">real</a> gifs]
<img class="gif" id="vibworld-gif" src="assets/gifs/vibworld.gif"/>
<img class="gif" id="hsv-gif" src="assets/gifs/RSS-banner-tunnel.gif"/>
<!-- [<a class="gif" href="#">gif<img class="preview" src="/assets/gifs/user_study.gif"></a>] -->

5.  [**Reactive Collision Avoidance using Real-Time Local Gaussian Mixture Model Maps**](/papers/IROS18.pdf)  
Aditya Dhawale, **Xuning Yang**, and Nathan Michael  
*International Conference on Intelligent Robots and Systems (IROS), October 2018*  
\[[bibtex](bibtex/iros18.txt)\]
[<a class="gif-link" id="iros18">gif</a>]
<img class="gif" id="iros18-gif" src="assets/gifs/iros18.gif"/>

6. [**Online adaptive teleoperation via motion primitives for mobile robots**](/papers/AURO18.pdf)  
**Xuning Yang**, Ayush Agrawal, Koushil Sreenath, and Nathan Michael  
*Special Issue on Learning for Human-Robot Collaboration, Autonomous Robots, April 2018*  
\[[bibtex](bibtex/auro18.txt)\]

7. [**A Framework for Efficient Teleoperation via Online Adaptation**](/papers/ICRA17.pdf)  
**Xuning Yang**, Koushil Sreenath, and Nathan Michael  
*International Conference on Robotics and Automation (ICRA), May 2017*  
\[[bibtex](bibtex/icra17.txt)\]
[<a class="gif-link" id="icra17">gif</a>]
<img class="gif" id="icra17-gif" src="assets/gifs/icra17.gif"/>

8.  [**Online Adaptive Teleoperation via Incremental Intent Modeling**](/papers/HRI17-LBR.pdf)  
**Xuning Yang**, Koushil Sreenath, and Nathan Michael  
*Late Breaking Report, International Conference on Human-Robot Interaction (HRI), March 2017*  
\[[bibtex](bibtex/hri17.txt)\]

<!-- ### Talks

1. Invited talk: Toward intuitive human controlled MAVs: motion primitives based teleoperation  
*IROS 2018 workshop: Vision based Drones: What's Next?* -->

### Other projects

1. In-place hover-to-hover flip of a quadrotor, featured in [Rapyuta Robotics Ltd. Teaser video](https://www.youtube.com/watch?v=zqp2Z2hbOFU-)  
[<a class="gif-link" id="flip">gif</a>]
<img class="gif" id="flip-gif" src="assets/gifs/flip_cropped.gif"/>

### Robots
I enjoy building robots. Some of the robots that are near and dear to my heart are listed here.
<div class="rowofposts">

{% for post in site.posts %}
  {% if post.category == "robot" %}

      {% include postbox-nosnippet.html %}
      {% endif %}
    {% endfor %}

</div>
