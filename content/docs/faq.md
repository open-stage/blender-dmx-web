---
title: Documentation and FAQ
menu:
  main:
    name: Docs / FAQ
    weight: 5
category: "Help"
---

<section class="uk-card uk-card-default">
    <div class="uk-card-body">
        <h2 class="uk-margin-top-large uk-card-title">New to BlenderDMX?</h2>
        <ul class="uk-list uk-list-bullet uk-list-primary">
            <li><strong><a href="/download" ><i class="fa-solid fa-download"></i>Downloading</a ></strong > and <strong><a href="/docs/installation" ><i class="fa-solid fa-download"></i>Installing</a ></strong > BlenderDMX.  </li>
            <li>Our <strong><a href="/docs/get_started" ><i class="fa-solid fa-rocket"></i> Getting Started Guide</a></strong> will get you
                up and running quickly.</li>
            <li>Looking for more comprehensive documentation? Continue reading the <strong><a href="../setup" ><i class="fa-solid fa-book"></i> User Guide</a></strong>.</li>
            <li>Need help troubleshooting the DMX integration? Check the
                <strong><a href="../dmx" ><i class="fa-solid fa-tachograph-digital"></i> DMX Integration</a></strong> section.</li>
            <li>Have more questions? Check out the <strong><a href="#faq-top" ><i class="fa-solid fa-circle-question"></i> FAQ</a></strong> or ask in the <strong><a rel="me" href="https://discord.gg/FQVVyc45T9"><i class="fa-brands fa-discord" aria-hidden="true"></i> Discord</a> </strong> group.</li>
        </ul>
        <h2 id="contribute" class="uk-card-title">Looking for ways to contribute?</h2>
        You can contribute to the project by sharing rendered visuals of your projects in the <a href="https://discord.gg/FQVVyc45T9">Gallery on Discord</a>, post rendered visuals on social media of your choice, <a href="https://github.com/open-stage/blender-dmx">writing code</a>, <a href="https://github.com/open-stage/blender-dmx-web/tree/main/content/docs">improving documentation</a>, or <a href="https://hosted.weblate.org/projects/blenderdmx/main/">help with translation</a>.
    </div>
</section>

<section id="faq-top">
<h2 class="uk-margin-large-top">Frequently Asked Questions</h2>
<h3>General</h3>
<ul uk-accordion="multiple: true">

<li>
<a id="faq_dmx" href="#faq_dmx" class="uk-accordion-title">What is DMX and do i need it?</a>
<div class="uk-accordion-content"> BlenderDMX is primarily a visualizing tool
for entertainment lighting, which typically is controlled by <a
href="../dmx">DMX protocol</a>. It is not strictly needed for BlenderDMX as you
can program by using <a href="../keyframe-animations-recording">keyframes</a>.
You can learn more about <a href="/docs/dmx">DMX here</a>.
</div>
</li>

<li> <a id="faq_blender" href="#faq_blender" class="uk-accordion-title">Can i use
Blender 2.9?</a> <div class="uk-accordion-content">No, you need to install <a
href="https://www.blender.org/download/">Blender</a> 3.4 or higher. Version 4.x
is supported but do note that when importing MVR files, Blender 4.x can be 10x
slower then Blender 3.x .
</div>
</li>

<li>
<a id="faq_error" href="#faq_error" class="uk-accordion-title">I get a random error, what should is do?</a>
<div class="uk-accordion-content">Oooups, this can happen. First, make sure you
use Blender 3.4 and higher, 4.x is also supported. If BlenderDMX is not working
for you at all, disable all other custom enabled addons to check for collision.
In BlenderDMX, set <a href="../setup/#logging">Logging</a> to Debug, this will
produce more information, saving it in the "blenderDMX.log" log file.
Replicate the action leading to the error, then look into the "blenderDMX.log"
logfile if you see anything obvious. Eventually, take the error message or the
full blenderDMX.log log file and ask in the <strong><a rel="me"
href="https://discord.gg/FQVVyc45T9"><i class="fa-brands fa-discord"
aria-hidden="true"></i> Discord</a> </strong> group.
</div>
</li>

<li>
<a id="faq_shortcuts" href="#faq_shortcuts" class="uk-accordion-title">Are there any special shortcuts in BlenderDMX?</a>
<div class="uk-accordion-content"> Yes, <a
href="../fixture/#navigation-between-fixtures">several</a>. You can use
Ctrl-Left / Ctrl-Right to go between fixtures (Previous/Next),
Ctrl-Shift-Left/Ctrl-Shift-Right to go between fixture's targets
(Previous/Next). When in the Fixtures list, you can use Shift to select
multiple fixtures.
</div>
</li>

<li>
<a id="faq_dmx_driver" href="#faq_dmx_driver" class="uk-accordion-title">Can i use DMX to control other parts of Blender?</a>
<div class="uk-accordion-content"> Yes. You can use our dedicated <a
href="../dmx#blenderdmx-dmx-driver-for-blender">DMX driver</a> for Blender to
use DMX as source of values for any Blender property.
</div>
</li>

<li>
<a id="faq_dmx_out" href="#faq_dmx_out" class="uk-accordion-title">Can BlenderDMX output DMX and be used as a DMX controller?</a>
<div class="uk-accordion-content">
This is currently not possible but if someone comes and implements this why not.
</div>
</li>

<li>
<a id="faq_mvr_import" href="#faq_mvr_import" class="uk-accordion-title">Can I import full MVR scene?</a>
<div class="uk-accordion-content">
Absolutely! Use the <a href="../setup/#import">Setup → Import → Import MVR Scene</a>. You can also use the
<a href="../gdtffixture/#mvr-xchange-protocol">MVR-xchange protocol</a> if you work with
another software which supports it.
</div>
</li>

<li>
<a id="faq_mvr_gdtf_empty" href="#faq_mvr_gdtf_empty" class="uk-accordion-title">After MVR import, GDTF fixtures have IDs and DMX but their bodies are not visible in 3D</a>
<div class="uk-accordion-content"> This depends on how you are doing the MVR
export in Vectoworks/Capture. Capture never provides any useful GDTFs, only
place-holders. Vectorworks provides useful GDTFs if you previously load them to
VW and link them to each VW symbol. To fix this issue, you can use the Edit
fixture function of BlenderDMX: after the MVR import to BlenderDMX, edit all
fixtures → uncheck the Re-address only and choose GDTF files for each fixture.
</div>
</li>

<li>
<a id="faq_gdtf_fixtures" href="#faq_gdtf_fixtures" class="uk-accordion-title">Why do fixtures from GDTF have different features, like Gobo or Color and some not?</a>
<div class="uk-accordion-content"> GDTF is a format to describe real world
devices, meaning that there are real lights out there which someone physically
built and uses on real stages. Some of them are simple with just a lamp, some
have colors, others may have gobos and pan/tilt and so on. If you don't care
about this, you can choose any fixture. See also the next question.
</div>
</li>

<li>
<a id="faq_spot_wash" href="#faq_spot_wash" class="uk-accordion-title">Is there a difference between Spot and Wash fixtures in BlenderDMX?</a>
<div class="uk-accordion-content"> Yes. BlenderDMX supports Spot, Wash, Beam,
Linear Strips, MultiPixel, Front Facing and other devices, including Lasers.
Spots have a hard beam edge, and if they contain gobos, their projection is
supported. Washes have a smooth blend on the beam. Narrow parallel beam angles
aligned with the front beam lens (beam fixtures) are also supported. Pixel
devices can be pixel controlled and any device can be set to not contain
volumetric beam to only provide front facing color mixing or strobing.
</div>
</li>

<li>
<a id="faq_lasers" href="#faq_lasers" class="uk-accordion-title">Are Lasers supported?</a>
<div class="uk-accordion-content">Yes. BlenderDMX allows to visualize laser
devices. The laser fixture definition is based on GDTF. By creating a custom
GDTF, there is a lot of flexibility of the types of lasers: single beam,
multiple beams, zooming, color changing, different shapes and so on. See
dedicated <a href="/docs/laser">Laser article</a> for details.</div>
</li>
<li>
<a id="faq_which_gdtf" href="#faq_which_gdtf" class="uk-accordion-title">What are good fixture files to start with?</a>
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

<li>
<a id="faq_cycles_eevee" href="#faq_cycles_eevee" class="uk-accordion-title">What is the difference between Cycles and Eevee?</a>
<div class="uk-accordion-content"> Blender has multiple rendering engines.
Eevee is a realtime renderer, while Cycles is an offline renderer that
calculates 3D data to produce realistic scenes. BlenderDMX has to implement
each feature two times, once for Eevee, once for Cycles. Saving keyframes is a
technique to prepare views and transitions for the Cycles renderer. Read about
Eevee and Cycles on the <a
href="https://duckduckgo.com/?t=ffab&q=what+is+the+difference+between+cycles+and+eevee">web</a>.
</div>
</li>

<li>
<a id="faq_gobos_cycles" href="#faq_gobos_cycles" class="uk-accordion-title">Instead of gobos i have pink beam output in Cycles</a>
<div class="uk-accordion-content">This seems as either some combination of
things or a bug in Blender. For some reason, Eevee has to be used at least once
with gobos, for gobos to render in Cycles. Simply switch the renderer to Eevee
and back to Cycles and gobos will show up.
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
