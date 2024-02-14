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
                <strong><a href="KeePassXC_GettingStarted.html#_setup_browser_integration" ><i class="fa-solid fa-globe"></i> DMX Integration</a></strong> section.</li>
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
<a id="faq-keepassx" href="#faq-keepassx" class="uk-accordion-title">Why KeePassXC instead of KeePassX?</a>
<div class="uk-accordion-content">
<p>KeePassX is no longer developed - as announced on the KeePassX website on 2021-12-09. Our decision to fork KeePassX
was made some years prior, due to a sharp decline in code frequency at the time, combined with our wish to provide
you with everything you love about KeePassX plus many new <a href="/#project">features and bugfixes</a>.</p>
</div>
</li>
<li>
<a id="faq-keepass" href="#faq-keepass" class="uk-accordion-title">Why KeePassXC instead of KeePass?</a>
<div class="uk-accordion-content">
<p>KeePass is a very proven and feature-rich password manager and there is nothing fundamentally wrong with it.
However, it is written in C# and therefore requires Microsoft's .NET platform.
On systems other than Windows, you can run KeePass using the Mono runtime libraries, but you won't get
the native look and feel which you are used to.</p>
<p>KeePassXC, on the other hand, is developed in C++ and runs natively on Linux, macOS and Windows giving you the
best-possible platform integration.</p>
</div>
</li>
<li>
<a id="faq-format" class="uk-accordion-title" href="#faq-format">Which password database formats are compatible with KeePassXC?</a>
<div class="uk-accordion-content">
<p>KeePassXC currently uses the KeePass 2.x (.kdbx) password database formats KDBX 3.1 and KDBX 4 as its native file formats.
KDBX 2 files can be opened, but will be upgraded to a newer format. KeePass 1.x (.kdb) databases can be imported into
a .kdbx file, but saving a .kdbx file as .kdb would be lossy, and saving to .kdb is not supported by KeePassXC.</p>
</div>
</li>
<li>
<a id="faq-cloudsync" class="uk-accordion-title" href="#faq-cloudsync">Why is there no cloud synchronization feature built into KeePassXC?</a>
<div class="uk-accordion-content">
<p>Cloud synchronization with Dropbox, Google Drive, OneDrive, ownCloud, Nextcloud etc. can be easily accomplished by
simply storing your KeePassXC database inside your shared cloud folder and letting your synchronization service of
choice do the rest. We prefer this approach, because it is simple, not tied to a specific cloud provider and keeps
the complexity of our code low.</p>
</div>
</li>
<li>
<a id="faq-general-plugins" class="uk-accordion-title" href="#faq-general-plugins">Does KeePassXC support (KeePass2) plugins?</a>
<div class="uk-accordion-content">
<p>No, KeePassXC does not support plugins at the moment and probably never will. KeePassXC already provides many of the features that
need third-party plugins in KeePass2, so for most things you don't even need plugins, nor should you ever want them.
Plugins are inherently dangerous. Many KeePass2 plugins are barely maintained (if at all), some have known vulnerabilities that
have never been (and probably never will be) fixed, and none of them are as thoroughly tested and reviewed as we test and review
code that goes into our main application. We find that encouraging users to install untested (and often quickly-abandoned) third-party
plugins is inherently incompatible with the security demands of a password manager.</p>

<p>If you really need external functionality not
available in KeePassXC, you can look for "plugins" that use the KeePassXC-Browser API, which is a much more secure way of sharing
passwords with third-party applications than loading those applications as plugins directly into KeePassXC.</p>
</div>
</li>
<li>
<a id="faq-general-wordlist" class="uk-accordion-title" href="#faq-general-wordlist">How can I add additional word lists to the passphrase generator?</a>
<div class="uk-accordion-content">
<p>You can add additional word lists to the passphrase generator by copying the word list file to the
<code>share/wordlists</code> folder inside your KeePassXC installation directory and then restarting KeePassXC.</p>

<p>On Linux, the default install location is <code>/usr/share/keepassxc</code>,
on macOS it is <code>/Applications/KeePassXC.app/Contents/Resources</code> and
on Windows <code>C:\Program Files\KeePassXC</code> (or <code>C:\Program Files (x86)\KeePassXC</code> for 32-bit).</p>
</div>
</li>

</ul>
<h3>Security</h3>
<ul uk-accordion="multiple: true">
<li>
<a id="faq-security-kdbx4" class="uk-accordion-title" href="#faq-security-kdbx4">How can I migrate my database to KDBX 4?</a>
<div class="uk-accordion-content">
<p>In the <em>Database</em> application menu, select <em>Database security...</em>. Select the <em>Encryption Settings</em> tab
and choose <em>KDBX 4.0 (recommended)</em>. Press OK and save the database.</p>
</div>
</li>
<li>
<a id="faq-security-totp" class="uk-accordion-title" href="#faq-security-totp">KeePassXC allows me to store my TOTP secrets.
Doesn't this undermine any advantage of two-factor authentication?</a>
<div class="uk-accordion-content">
<p>Yes. But only if you store them in the same database as your password. We believe that storing both together
can still be more secure than not using 2FA at all, but to maximize the security gain from using 2FA,
you should always store TOTP secrets in a separate database, secured with a different password, possibly even on a different computer.</p>
</div>
</li>
<li>
<a id="faq-security-why-pm" class="uk-accordion-title" href="#faq-security-why-pm">Why would I use a password manager? Isn't it totally insecure to use
one password for everything?</a>
<div class="uk-accordion-content">
<p>Password reuse and simple, easy-to-guess passwords are the biggest problems when using online services.
If one service gets compromised (either by guessing your password or by exploiting a security vulnerability
in the service's infrastructure), an attacker may gain access to all of your other accounts.</p>

<p>But using different passwords for all websites is difficult without a way of storing them somewhere safe.
Especially with arbitrary password rules for various services, it becomes increasingly hard to use both strong
and diverse passwords. KeePassXC stores your passwords for you in an encrypted database file, so you only
need to remember one master password. Of course, the security of all your services depends on the strength
of your master password now, but with a sufficiently strong password, the password database should be
infeasible to crack.</p>

<p>The database is encrypted with either the industry-standard AES256 or the Twofish
block cipher and the master password is strengthened by a configurable number of key transformations
to harden it against brute force attacks. Additionally, you can use a key file filled with an arbitrary
number of random bytes or a YubiKey to further enhance your master key.</p>
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
