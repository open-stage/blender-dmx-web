---
title: Documentation and FAQ
menu:
  main:
    name: Docs / FAQ
    weight: 5
---

<section class="uk-card uk-card-default">
    <div class="uk-card-body">
        <h2 class="uk-margin-top-large uk-card-title">New to BlenderDMX?</h2>
        <ul class="uk-list uk-list-bullet uk-list-primary">
            <li><strong><a href="/download" ><i class="fa-solid fa-download"></i>Downloading</a ></strong > and <strong><a href="/docs/installation" ><i class="fa-solid fa-download"></i>Installing</a ></strong > BlenderDMX.  </li>
            <li>Our <strong><a href="/docs/get_started" ><i class="fa-solid fa-rocket"></i> Getting Started Guide</a></strong> will get you
                up and running quickly.</li>
            <li>Looking for more comprehensive documentation? Our <strong><a href="/docs/user_guide" ><i class="fa-solid fa-book"></i> User Guide</a></strong> is there to help.</li>
            <li>Need help troubleshooting the DMX integration? Check the
                <strong><a href="../dmx" ><i class="fa-solid fa-globe"></i> DMX Integration</a></strong> section.</li>
        </ul>
        <h2 id="contribute" class="uk-card-title">Looking for ways to contribute?</h2>
        You can contribute to the project by sharing rendered visuals of your projects in the <a href="https://discord.gg/FQVVyc45T9">Gallery on Discord</a>, post rendered visuals on social media of your choice, <a href="https://github.com/open-stage/blender-dmx">writing code</a>, or <a href="https://github.com/open-stage/blender-dmx">improving documentations</a>.
    </div>
</section>

<section id="faq">
<h2 class="uk-margin-large-top">Frequently Asked Questions</h2>
<h3>General</h3>
<ul uk-accordion="multiple: true">
<li>
<a id="faq" href="#faq" class="uk-accordion-title">What is DMX and do i need it?</a>
<div class="uk-accordion-content">
BlenderDMX is primarily a visualizing tool for entertainment lighting, which
typically is controlled by DMX protocol. It is not strictly needed for
BlenderDMX as you can program by using keyframes.
You can learn more about <a href="/docs/dmx">DMX here</a>.
</div>
</li>
<li>
<a id="faq" href="#faq" class="uk-accordion-title">What are good fixture files to start with?</a>
<div class="uk-accordion-content">
<p>While the fixture definitions in GDTF describe and mimic real lighting
devices, if you have no idea about entertainment lighting and just want to do
something creative in Blender, you might not care about what light you use and
just need some fixtures to play around with. One of the companies defining GDTF
specification and providing well prepared GDTF files is Robe Lighting, their
fixture files use correct, use 3D models in glb format with defined material,
gobos are with correct transparency and the DMX description works well. There
are also other manufacturers and fixtures files, check out the GDTF Share for
more.
</p>
</div>
</li>


</ul>

</section>

<script type="module">
    $(() => {
        if (location.hash) {
            $(':target').each((i, e) => {
                if (e.id === location.hash.substring(1)) {
                    UIkit.accordion(e.parentNode.parentNode).toggle(e.parentNode, true);
                }
            });
        }
    });
</script>
