**Дисципліна:** Основи побудови інформаційних систем та мереж

**Тема:** Спостереження за процесом звернення до вебресурсу. Побудова власної моделі рівнів взаємодії

| | |
|---|---|
| **Прізвище, ім'я** | Сависько Назір |
| **Група** | ІПЗ-2.01 |
| **Номер варіанта** | 24 |
| **Домен варіанта** | tug.org |
| **Середовище виконання** | Linux |
| **Версія curl** | curl 8.18.0 (x86_64-pc-linux-gnu) libcurl/8.18.0 OpenSSL/3.5.5 zlib/1.3.1 brotli/1.2.0 zstd/1.5.7 libidn2/2.3.8 libpsl/0.21.2 libssh2/1.11.1 nghttp2/1.68.0 librtmp/2.3 mit-krb5/1.22.1 OpenLDAP/2.6.10 |
| **Дата виконання** | 09.09.2026, 20.09.2026 |

---

## Частина A. Збір експериментальних даних

### A.1. Запит із діагностичним виводом

**Команда:**

```
curl -v https://tug.org
```

**Вивід:**

```
  % Total    % Received % Xferd  Average Speed  Time    Time    Time   Current
                                 Dload  Upload  Total   Spent   Left   Speed
  0      0   0      0   0      0      0      0                              0* Host tug.org:443 was resolved.
* IPv6: (none)
* IPv4: 46.4.94.215
*   Trying 46.4.94.215:443...
* ALPN: curl offers h2,http/1.1
} [5 bytes data]
* TLSv1.3 (OUT), TLS handshake, Client hello (1):
} [1562 bytes data]
* SSL Trust Anchors:
*   CAfile: /etc/ssl/certs/ca-certificates.crt
*   CApath: /etc/ssl/certs
{ [5 bytes data]
* TLSv1.3 (IN), TLS handshake, Server hello (2):
{ [122 bytes data]
* TLSv1.3 (IN), TLS change cipher, Change cipher spec (1):
{ [1 bytes data]
* TLSv1.3 (IN), TLS handshake, Encrypted Extensions (8):
{ [25 bytes data]
* TLSv1.3 (IN), TLS handshake, Certificate (11):
{ [5859 bytes data]
* TLSv1.3 (IN), TLS handshake, CERT verify (15):
{ [520 bytes data]
* TLSv1.3 (IN), TLS handshake, Finished (20):
{ [52 bytes data]
* TLSv1.3 (OUT), TLS change cipher, Change cipher spec (1):
} [1 bytes data]
* TLSv1.3 (OUT), TLS handshake, Finished (20):
} [52 bytes data]
* SSL connection using TLSv1.3 / TLS_AES_256_GCM_SHA384 / x25519 / RSASSA-PSS
* ALPN: server accepted http/1.1
* Server certificate:
*   subject: CN=tug.org
*   start date: Aug 20 22:13:36 2026 GMT
*   expire date: Nov 18 22:13:35 2026 GMT
*   issuer: C=US; O=Let's Encrypt; CN=YR1
*   Certificate level 0: Public key type RSA (4096/152 Bits/secBits), signed using sha256WithRSAEncryption
*   Certificate level 1: Public key type RSA (2048/112 Bits/secBits), signed using sha256WithRSAEncryption
*   Certificate level 2: Public key type RSA (4096/152 Bits/secBits), signed using sha256WithRSAEncryption
*   Certificate level 3: Public key type RSA (4096/152 Bits/secBits), signed using sha256WithRSAEncryption
*   subjectAltName: "tug.org" matches cert's "tug.org"
* SSL certificate verified via OpenSSL.
* Established connection to tug.org (46.4.94.215 port 443) from 192.168.10.152 port 34660 
* using HTTP/1.x
} [5 bytes data]
> GET / HTTP/1.1
> Host: tug.org
> User-Agent: curl/8.18.0
> Accept: */*
> 
* Request completely sent off
{ [5 bytes data]
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
{ [57 bytes data]
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
{ [57 bytes data]
< HTTP/1.1 200 OK
< Date: Wed, 09 Sep 2026 08:03:35 GMT
< Server: Apache/2.4.68 (Unix) OpenSSL/1.1.1k
< Upgrade: h2
< Connection: Upgrade
< Accept-Ranges: bytes
< Transfer-Encoding: chunked
< Content-Type: text/html
< 
{ [5 bytes data]
<!-- $Id: header.html,v 1.3 2025/07/14 17:33:41 karl Exp $ -->
<!DOCTYPE html>
<html lang="en"><head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<link rel="stylesheet" href="/tugstyle.css">

<meta name="color-scheme" content="light dark">
<style>
@media (prefers-color-scheme: dark) {
  *, *::before, *::after {
    background-color: revert !important;
    color: revert !important;
 }
}
</style>
<!-- end header -->

<!-- $Id: index.html,v 1.1393 2026/09/01 20:49:07 karl Exp $ -->
<title>TeX Users Group (TUG)</title>
<link rel="stylesheet" href="homestyle.css">
</head>
<body>
<div class="topbar">
  <div class="logo">
    <a href="/forms/current/memberapp.html">
    <input style="border:none; margin:0; padding:0;"
           type="image" width=80 height=92 src="/images/tuglogo.png"
           border=0 alt="Join the TeX Users Group"></a>
  </div>
  <form class="search" method=get action="//duckduckgo.com/">
    <input type="hidden" name="sites" value="tug.org"
    ><input name=q xsize=12 maxlength=99 placeholder="Search tug.org"
    ><input type=submit value="Find">
    <br><small>(via&nbsp;<a href="https://www.duckduckgo.com/"
                         >DuckDuckGo</a>)</small>
  </form>

  <div class="tugtitle">
  <h2><span class="TEX">T<span class="E">E</span>X</span
      >&nbsp;Users&nbsp;Group</h2>

   <div class="buttons">
    <a href="/forms/current/memberapp.html">
    <input style="border:none; margin:0; padding:0;"
           type="image" width=131 height=40 src="/images/btn_join_renew.png"
           border=0 alt="Join the TeX Users Group"></a>
    <!-- here is the renew button, has to be a form for paypal: -->
    <form style="display:inline; border:none; margin:0; padding:0;"
          action="https://www.paypal.com/cgi-bin/webscr"
          method="post" target="_top">
    <input type="hidden" name="cmd" value="_s-xclick">
    <input type="hidden" name="hosted_button_id" value="D6VKGM9GBQ4TU">
    &nbsp;&nbsp;
    <input type="image" width=89 height=38 src="/images/btn_donate.png"
           border=0 name="submit" style="padding-bottom:2px;"
           alt="Donate via PayPal to the TeX Users Group">
    </form>
   </div><!-- end buttons -->
  </div><!-- end tugtitle -->
</div><!-- end topbar -->

<div class="main-container">
<!-- emacs-page -->
<section class="main">

<p><b>The TeX Users Group (TUG)</b> is a membership-based not-for-profit
organization, founded in 1980, for anyone who uses the TeX typesetting
system created by <a
href="https://www-cs-faculty.stanford.edu/~knuth/">Donald&nbsp;Knuth</a>
and/or is interested in typography and font design.

<p><a href="/forms/current/memberapp.html"><b>Join or
renew with TUG</b></a>
(<a href="/forms/current/trialapp.html">trial
memberships</a> available for new members)
to support use and development of TeX and friends.  All TUG memberships
are for the calendar year, and include all benefits for the year no
matter when you join.

<p id="new">If you're <a href="/begin.html"><b>new to TeX</b></a>, we
recommend installing TeX&nbsp;Live (<a
href="/texlive/windows.html">Windows</a>, <a
href="/mactex/mactex-download.html">macOS</a>, <a
href="/texlive/quickinstall.html">GNU/Linux/Unix</a>). The <a
href="https://www.learnlatex.org/">Learn LaTeX</a> site provides an
interactive online tutorial for creating documents with LaTeX. Our <a
href="/begin.html">getting started page</a> contains additional
resources for beginners.

<p id="help"><b>If you're looking for help</b>, you can get community
support via:
<a href="https://tex.stackexchange.com/" rel="nofollow">q&amp;a site</a>
  (tex.stackexchange.com),
<a href="https://latex.org/forum/">forum</a>&nbsp;(latex.org), 
<a href="https://lists.tug.org/texhax">public mailing list</a> (texhax@tug.org),
<a href="https://www.reddit.com/r/LaTeX/">reddit</a>,
and <a href="/interest.html#doc">in other ways</a>.

<p><a href="https://lists.tug.org/tex-announce"><b>Subscribe to our
monthly newsletter</b></a> if you like (open to all,
automatically sent to members).

<!-- enable at beginning/end of year -->
<!-- include virtual="/i/begging.html"-->

<!-- emacs-page -->
<hr>
<p id="news">
<font color="8B0000"><b>News</b></font>
<small>(<a href="https://tex.social/">blogs</a>)</small>
<a href="http://tug.org/rss/tug.xml"><img
  src="/rss/xml.png" width=36 height=14 alt="TUG RSS feed"></a>

<p class="negskip">
<ul>
<li><b><a href="/TUGboat/tb47-2/">TUGboat 47:2</a></b>,
      the <a href="/tug2026/">TUG'26</a> proceedings,
      is available online and from the <a href="/store/#tugboat">TUG store</a>,
      and will be mailed to current TUG members soon.
    <!-- <a href="/l/tug25-wholeday">Whole-day videos for TUG'25</a> are
      available; videos for invidual talks will be posted when available. -->
    In addition, prior TUGboat issue
      <a href="/TUGboat/tb47-1/">47:1</a> is now publicly available.
    <!-- The next issue will be the <a href="/tug2026/">TUG'26</a>
      proceedings; the deadline for papers to be
      included there is July&nbsp;26, 2026. -->
      <!-- Presentation proposals for the conference, including for
           remote presentations, continue to be welcome; see the
           <a href="/tug2026/cfp.html">call for papers</a>. -->
    <a href="/TUGboat/location.html">Submissions for the next regular
      issue</a> are welcome and encouraged; the deadline
      is October&nbsp;23, 2026.

<li><b><a href="/books/#reviews">New book review:</a></b>
    <a href="/books/reviews/tb146reviews-kottwitz-beginners3.html"
    >LaTeX Beginner's Guide, third edition</a>, by Stefan Kottwitz,
    reviewed by Uwe Ziegenhagen.

<li><b><a href="/texlive/">TeX Live 2026</a> and <a
    href="/mactex/">MacTeX 2026</a></b> have been released.
    They are primarily distributed online through <a
    href="https://ctan.org/">CTAN</a>. More info:
    <a href="https://ctan.org/pkg/texlive">TL</a>,
    <a href="https://ctan.org/pkg/mactex">MacTeX</a>.

<!-- <li><b><a href="/join.html">TUG membership forms for 2026</a></b> are
    available for your joining/renewing pleasure (automatic renewals
    are underway). Early bird rate ends on April&nbsp;4, so
    don't hesitate to join or renew. For anyone new to TUG, we offer a <a
    href="/forms/current/trialapp.html">trial membership</a> with full
    benefits for&nbsp;$35, or without printed journals for &nbsp;$20. -->

<li><b><a href="publicity/membership_poster_math/">A new TUG membership
    poster</a></b> is available; it's oriented towards STEM departments and
    organizations. We greatly appreciate any posts, electronically or
    physically, of this one-page flyer.
    
<!-- <li><b><a href="/interviews/cain.pdf">Alan&nbsp;J. Cain</a></b>,
    author of <a href=
    "https://archive.org/details/cain_formandnumber_ebook_large" >Form
    &amp; Number: A History of Mathematical Beauty</a>, is the latest
    subject in TUG's <a href="/interviews/">Interview Corner</a>. It
    will also be published in the next TUGboat issue (submissions always
    welcome). -->

<!-- <li><b><a href="/texlive/pretest.html">The TeX Live 2027 pretest</a></b>
    is continuing, with the release approaching. If anyone
    would like to help test the upcoming release, please try it now.

<!-- <li><b><a href="/election/">TUG 2025 election results</a></b> are
    available online and will be printed in the next TUGboat. There is
    no need for a ballot this year. Many thanks and congratulations to
    the continuing (as of the <a href="/tug2025/">TUG&nbsp;2025
    conference</a>) president Arthur Rosendahl, and new board members
    Doris&nbsp;Behrendt and Erik&nbsp;Nijenhuis.
    Many thanks also to Ross Moore,
    who is stepping down at the end of this term after many years of
    service. -->

</ul>

<!-- emacs-page -->
<p id="events"><font color="8B0000"><b>Upcoming events</b></font>
(<a href="meetings.html">meeting list</a>)
<p class="negskip">
<ul>
<li><b><a href="https://www.dante.de/veranstaltungen/#herbst2026"
  >DANTE autumn meeting</a></b>, Sept.&nbsp;25-26, 2026, Ordix&nbsp;IT.
  Short general meeting on Sept.&nbsp;26th.

<li><b><a href="https://www.unicode.org/events/utw/2026/program/"
  >Unicode Technology Workshop</a></b>: Unicode in the World,
  October&nbsp;20-23, 2026, Atelier National de Recherche Typographique
  (ANRT), Nancy, France. Tutorials on Oct 20-21, talks on Oct 22-23.
  Tickets available for partial or full days.

<li><b><a href="https://www.dante.de/veranstaltungen/"
  >DANTE spring 2027 meeting</a></b>, April&nbsp;8-10, 2027, University
  of Ulm, Germany; tutorials, introduction, reception on April&nbsp;7.
  General meeting on April&nbsp;10.

<li id="tug27"><b><a href="/tug2027/">TUG 2027</a></b>,
  will be held in Paris (France), in the summer; dates and
  location will be announced as soon as they are known.

</ul>

<font color="8B0000"><b>Recent events</b></font>
<p class="negskip">
<ul>
<li><b><a href="https://meeting.contextgarden.net/2026/">ConTeXt
  Meeting 2026</a></b>: Maibach, Germany, August 24-29, 2026,
  Theme: &ldquo;Focussing&rdquo;. (Other topics also welcome!)

<li id="tug26"><b><a href="/tug2026/">TUG 2026</a></b>,
   <a href=
     "https://www.germainhotels.com/en/alt-hotel/calgary-east-village">
  Alt Hotel Calgary East Village</a>, Calgary, Canada,
  July 17-19 (Friday-Sunday),
  with a <a href="tug2026/workshop.html">LaTeX developers' workshop</a>
  with a LaTeX developers' workshop
  on Thursday, July&nbsp;16.
  <a href="/l/tug26-video">Videos for all TUG'26 talks</a> are
      available.
  <!-- The registration form and more information will be posted when
      available. -->
  <!-- <br>The <a href="https://youtube.com/c/texusersgroup/live"
      >YouTube Live</a> stream is available. Videos for individual talks
      will be available as soon as possible. -->
      <!-- , starting Friday 08:55 CEST. The
      conference is streamed at no charge and no online
      registration is necessary; <a href="/donate.html">donations</a>
      are greatly appreciated to help defray the cost. -->
  <!-- <br><a href="/tug2026/travel.html">Visa/etravel application</a> is
      advised to be started as soon as possible. -->
  <!-- <br><a href="/bursary/2026app.html">Bursary application available</a
       >&nbsp;(for financial&nbsp;assistance): deadline April&nbsp;3. -->
  <!-- <br><a href="/tug2026/register.html">Register for the
       conference</a>: early bird deadline April&nbsp;24. -->
  <!-- <br><a href="/tug2026/cfp.html">Call for papers</a>: deadline
       April&nbsp;24; -->
       <!-- while early submissions are greatly appreciated. -->
       <!-- that initial deadline has passed, but we will continue to
       gratefully accept submissions as long as the schedule remains open.
       This will primarily be an in-person conference,
       but remote presentations are welcome. -->
  <!-- <br><a href="/tug2026/#hotel">Hotel reservations</a>: 
       deadline June&nbsp;16; booking early is highly advisable. -->

<li><b><a href="https://ossconf.fri.uniza.sk/"
  >OSSConf 2026</a></b>, July&nbsp;1-3, 2026, at the University of
  &#x017D;ilina, Slovakia, will have a dedicated TeX+R session,
  and several TeX-related workshops.
  The conference will be multilingual, but primarily in Czech and Slovak.
  Documents in English:
  <a href=
"https://ossconf.fri.uniza.sk/wp-content/uploads/2026/03/OSSConf2026-invitation.pdf"
  >Conference invitation</a>;
  <a href=
"https://invimath.fri.uniza.sk/images/slides/OSSConf/plagatOSS_2026-EN.pdf"
  >poster</a>;
  <a href=
"https://ossconf.fri.uniza.sk/wp-content/uploads/2026/03/ossconf-whyr.pdf"
  >Bridging the gap: R, LaTeX, and the Future of Open Source at OSSConf
  2026</a>, a one page description of the conference, including the LaTeX
  document engineering track.

<li><b><a href="https://pdfa.org/event/webinar-accessible-mathematical-content-in-pdf/"
    >Webinar - Accessible Mathematical Content in PDF</a></b> presented
    June&nbsp;16 by LaTeX team members and colleagues is available from the <a
    href="https://pdfa.org">PDF Association</a> web site. The web site
    provides many related resources available as well.

<li><b><a href="https://bachotex.gust.org.pl/index_en.html">EuroBachoTeX
2026</a></b>, in Bachotek, Poland, April&nbsp;29-May&nbsp;3, 2026.
This year's theme: &ldquo;TeX vs. AI&rdquo;:
<a href="https://bachotex.gust.org.pl/2026/cfp_en.html">Call for papers</a>;
<a href="https://bachotex.gust.org.pl/2026/register_en.html"
  >registration form</a>;
<a href="https://bachotex.gust.org.pl/2026/payment_en.html"
  >fees and financial info</a>;
<a href="https://tug.org/pipermail/texhax/2026-March/026957.html"
  >announcement</a>.

<li><b><a href="https://principiae.be/register/X0500.php"
  >Structuring your research story</a></b>, a talk by Jean-luc Doumont
  of <a href="https://principiae.be">Principiae</a>, March&nbsp;31,
  2026, 19:45 to 22:00 in Leuven (campus Gasthuisberg), Belgium. No
  charge, in-person only.

<li><b><a href="https://seminarseries.muni.cz/mathematics-physics-computer-science/lectures/%CF%84%CE%AD%CF%87%CE%BD%CE%B7-gutenberg-knuth-zapf-lamport-latex-the-evolution-of-document-production-and-information-access"
  >Gutenberg - Knuth - Zapf - Lamport - LaTeX</a></b>, March&nbsp;19, 2026:
  Frank Mittelbach will receive an honorary doctorate from Masaryk
  University Brno for his life's work on research in document
  engineering and making LaTeX what it is today. The ceremony will be in
  the morning and he will give a talk in the afternoon. Both events are
  open to the public. Congratulations, Frank!

<li><a href="https://jointmathematicsmeetings.org/meetings/national/jmm2026/jmm2026-speakers"
><b>The Shape of Letters:</b></a> <i>From Leonardo da Vinci to Donald
  Knuth</i>, an invited talk (Jan.&nbsp;4) by &Eacute;tienne&nbsp;Ghys at
  the Joint Mathematics Meetings, January&nbsp;4-7, 2026, Washington DC.

<!-- <li><b><a href="https://www.gutenberg-asso.fr/-Exposes-mensuels-">GUTenberg
  Expos&eacute;s mensuels</a></b>, online video presentations, in French:
  <ul>
  </ul>

<li><b><a href="https://www.gutenberg-asso.fr/Assemblee-generale-du-16-novembre-2025"
  >GUTenberg general assembly</a></b>, online,
  November&nbsp;16, 2025 at 3&nbsp;p.m.
  <ul>
  <li>December&nbsp;4, 2025, Valentin Dao
  will give a <a href="https://www.gutenberg-asso.fr/4-decembre-2025-Presentation-du-package-intexgral-et-de-la-syntaxe-expl3"
  >presentation</a> on his <a 
  href="https://ctan.org/pkg/intexgral">intexgral</a> package and expl3
  syntax.
  <li>
  January 8, 2026, Jean Abou Samra will give a
  <a href="https://www.gutenberg-asso.fr/Logiciel-de-gravure-musicale-Lilypond"
  >presentation</a> on <a href="https://lilypond.org/">Lilypond</a>.
  </ul>
  
<li><b><a href="https://www.guitex.org/home/en/meeting">GuIT
  2025</a></b>, Pisa, Italy, November&nbsp;5, 2025.

<li><b><a href="https://www.gutenberg-asso.fr/Journee-GUTenberg-2025"
  >Journe&eacute; GUTenberg 2025</a></b> annual meeting,
  &Eacute;cole normale sup&eacute;rieure, Paris,
  November&nbsp;8, 2025.

<li><b><a href="https://www.gutenberg-asso.fr/-Exposes-mensuels-">GUTenberg:
  Expos&eacute;s mensuels</a></b>, online, September&nbsp;10, 2025.
  Videoconference, in French, by Didier Verna on &ldquo;Traitement des
  probl&egrave;mes de similarit&eacute; dans la justification de
  paragraphe&nbsp;: une extension du Knuth-Plass&rdquo;.

-->

</ul>

<!-- emacs-page -->
<p><hr size=1 noshade>
<b>TUG is a not-for-profit organization by, for, and of its
members</b>, also representing the interests of TeX users worldwide.
If you use any TeX-related programs (TeX, <a
href="http://www.latex-project.org/">LaTeX</a>, <a
href="http://www.contextgarden.net/">ConTeXt</a>, <a
href="http://www.math.utah.edu/~beebe/fonts/metafont.html">Metafont</a>,
<a href="/metapost.html">MetaPost</a>, <a
href="http://www.gnu.org/software/texinfo/">Texinfo</a>, <a
href="/interest.html">et al.</a>), please consider <a
href="/join.html">joining TUG</a> (or <a href="/usergroups.html">another
TeX user group</a>).
<a href="/join.html">Memberships</a> and <a
href="/donate.html">donations</a> are <a
href="/tax-exempt/">tax-deductible</a> in the US.

<p><b><a href="/aims_ben.html">TUG membership benefits</a></b> include
our journal <a href="/TUGboat"><i>TUGboat</i></a> (available both in
print and online). TUG also runs an <a href="meetings.html">annual TeX
conference</a>, and supports updates to the <a
href="/texcollection/">TeX Collection</a> software: <a
href="/texlive/">TeX&nbsp;Live</a>, <a href="/mactex/">MacTeX</a>, <a
href="https://ctan.org/">snapshot of CTAN</a>, among other activities.

<!-- emacs-page -->
<p><hr size=1 noshade>
<b>The <a href="https://ctan.org/">Comprehensive TeX Archive Network</a>
(CTAN)</b> is the primary repository for TeX-related software on the
Internet. CTAN has many thousands of items; its
<a href="https://ctan.org/pkg/">package&nbsp;list</a>, 
<a href="https://ctan.org/topics/cloud">topic&nbsp;cloud</a>, and
<a href="https://ctan.org/search.html">CTAN search page</a> can help you
find what you need.

<p><font color="8B0000"><b>Latest <a href="https://ctan.org/">CTAN</a>
updates</b></font>
<a href="https://ctan.org/ctan-ann/rss"><img
  src="/rss/xml.png" width=36 height=14 alt="CTAN RSS feed"></a>
- <a href="https://www.ctan.org/ctan-ann/id/f50298e997f073db@hogwart">mtp2otf</a>
- <a href="https://www.ctan.org/ctan-ann/id/f50298e4cc3d88b8@hogwart">ciad-beamertheme</a>
- <a href="https://www.ctan.org/ctan-ann/id/aqBbuSNTQQyMp1SJ@prptp">numodel-bundle</a>
- <a href="https://www.ctan.org/ctan-ann/id/ba4a4bf5-cebb-afa1-ec7d-87fa52a6b1a3@tantalus.jena.thur.de">mahjong-tiles@uni-jena.de;&nbsp;(fwd)</a>
- <a href="https://www.ctan.org/ctan-ann/id/ed225b4b-6bc1-c74a-1d4e-322508db3dc5@ctan.org">hicite</a>
- <a href="https://www.ctan.org/ctan-ann/id/21696467-b5cd-66af-dcf2-434ff29f5f0e@ctan.org">luamplib</a>
- <a href="https://www.ctan.org/ctan-ann/id/69da28d1-706e-3fa3-43b9-aea58d9a6473@ctan.org">mahjong-tiles@uni-jena.de;</a>
- <a href="https://www.ctan.org/ctan-ann/id/ap-0_kaciSd-y0eI@prptp">malagasy-numberwords</a>
- <a href="https://www.ctan.org/ctan-ann/id/ap5kwj3C0ngCH0A7@prptp">luadraw</a>
- <a href="https://www.ctan.org/ctan-ann/id/ap2zY0Fc6O1bIozC@prptp">siunitx</a>
- <a href="https://www.ctan.org/ctan-ann/id/707ca6bb-a979-7741-d3ae-01edcb9a3f41@ctan.org">latex-tagging-status</a>
- <a href="https://www.ctan.org/ctan-ann/id/ap0OWT5coQC3otfb@prptp">tikzphysics</a>
- <a href="https://www.ctan.org/ctan-ann/id/4de363e6-0921-3855-a733-bcb9a4a4f98b@ctan.org">codebox</a>
- <a href="https://www.ctan.org/ctan-ann/id/apqYFQlLZ9djqq7n@prptp">TIETreport</a>
- <a href="https://www.ctan.org/ctan-ann/id/edda8cde-56e8-9c34-26be-34786a5d22d0@ctan.org">suanpan-l3</a>
- <a href="https://www.ctan.org/ctan-ann/id/45028cbd-13f1-926c-dd2c-0265e2b02881@ctan.org">chinesechess</a>
- <a href="https://www.ctan.org/ctan-ann/id/ae51d6b02308a29b@hogwart">dtk-bibliography</a>
- <a href="https://www.ctan.org/ctan-ann/id/ae51d6ab9ed99062@hogwart">hawkdraw</a>
- <a href="https://www.ctan.org/ctan-ann/id/ae51d6a634c8852c@hogwart">chemidentifier</a>
- <a href="https://www.ctan.org/ctan-ann/id/apnDYmwLrqIR9pwH@prptp">multicoltab</a>
- <a href="https://www.ctan.org/ctan-ann/id/00c1d629-8d2e-9f02-13e2-5369f1363a37@ctan.org">mahjonggame</a>
- <a href="https://www.ctan.org/ctan-ann/id/0b35dd0b-d728-0403-ef6e-8fe916d83009@ctan.org">ltx-talk</a>
- <a href="https://www.ctan.org/ctan-ann/id/aphv_xEzFQo9a-ma@prptp">FantasqueSansMono-OTF</a>
- <a href="https://www.ctan.org/ctan-ann/id/ae51d67460fd491a@hogwart">RetosMatematicos</a>
- <a href="https://www.ctan.org/ctan-ann/id/aphaPhOoYUghJSrA@prptp">chemfig</a>
- <a href="https://www.ctan.org/ctan-ann/id/aphF42zKl556FlyC@prptp">l3build</a>
- <a href="https://www.ctan.org/ctan-ann/id/f3e51d52584b56b3@hogwart">jss-lint</a>
- <a href="https://www.ctan.org/ctan-ann/id/apbv53vgaPdMZjz9@prptp">babel-malagasy</a>


</section>

 <aside class="navbar">
  <font color="8B0000"><b>TUG&nbsp;membership</b></font><br>
  <a href="/join.html">Join/renew&nbsp;with&nbsp;TUG</a><br>
  <a href="/members/">TUG&nbsp;member&nbsp;area</a><br>
  <a href="/instmem.html">Institutional&nbsp;members</a><br>
  &nbsp;<br>

  <font color="8B0000"><b>About&nbsp;TUG</b></font><br>
  <a href="/contact.html">Contact&nbsp;us</a><br>
100  24051   0  24051   0      0  45411      0                              0
* Connection #0 to host tug.org:443 left intact
sp;a&nbsp;donation</a><br>
  <a href="/tax-exempt/">Tax&nbsp;exempt</a><br>
  <a href="/aims_ben.html">Aims&nbsp;&amp;&nbsp;benefits</a><br>
  <a href="/board.html">Board</a>,&nbsp;<a
     href="/committees.html">Committees</a><br>
  <a href="/election/">Elections</a><br>
  &nbsp;<br>

  <font color="8B0000"><b>New&nbsp;to&nbsp;TeX?</b></font><br>
  <a href="/begin.html">Getting&nbsp;started</a><br>
  <a href="https://texfaq.org/">FAQ</a><br>
  <a href="/whatis.html">History&nbsp;of&nbsp;TeX</a><br>
  &nbsp;<br>

  <font color="8B0000"><b>Software</b></font><br>
  <a href="https://ctan.org/">Downloads/CTAN</a><br>
  <a href="/texlive/">TeX&nbsp;Live</a>&nbsp;-&nbsp;<a href="/mactex/">MacTeX</a><br>
  <a href="https://miktex.org/">MiKTeX</a><br>
  <!-- <a href="/applications/">(La)TeX&nbsp;projects</a><br> -->
  <a href="/interest.html">TeX&nbsp;around&nbsp;the&nbsp;web</a><br>
  &nbsp;<br>

  <font color="8B0000"><b>TUG&nbsp;activities</b></font><br>
  <a href="/TUGboat/">TUGboat</a><br>
  <a href="/tc/devfund/">Project&nbsp;funding</a><br>
  <a href="/books/">Bookstore/reviews</a><br>
  <a href="/store/">TUG&nbsp;store</a><br>
  <a href="/store/lucida/">Lucida&nbsp;fonts</a><br>
  <a href="/interviews/">Interviews</a><br>
  &nbsp;<br>

  <font color="8B0000"><b>TeX worldwide</b></font><br>
  <a href="/usergroups.html">User&nbsp;groups</a><br>
  <a href="/meetings.html">Conferences</a><br>
  <a href="/pubs/">Journals/Publications</a><br>
  <a href="/mailman/listinfo">Mailing&nbsp;lists</a><br>
  <a href="/twg.html">Working&nbsp;groups</a><br>
  <a href="/publicity/">Stickers&nbsp;&amp;&nbsp;publicity</a><br>
  &nbsp;<br>

  <font color="8B0000"><b>Typography</b></font><br>
  <a href="/FontCatalogue/">Font&nbsp;Catalogue</a>
  <a href="/texshowcase/">TeX&nbsp;showcase</a><br>
  <a href="/fonts/">Fonts&nbsp;for&nbsp;TeX</a><br>
  <a href="/video.html">Videos</a><br>
  <a href="/museums.html">Typography&nbsp;museums</a><br>
  &nbsp;<br>

  <font color="8B0000"><b>Jobs</b></font><br>
  <a href="/consultants.html">Consultants&nbsp;for&nbsp;hire</a><br>
  <a href="/jobboard.html">Job&nbsp;openings</a><br>
 </aside>

</div> <!-- end main-container -->

<!-- emacs-page -->
<hr size=1 noshade>
<p id="ctan">
<font color="8B0000"><b>Contact Us</b></font>

<table cellpadding=10>
<tr valign=top><td width="30%"><small>
       <b>TeX Users Group<br>
          PO Box 2311<br>
          Portland, OR 97208-2311<br>
          USA<br>
       </b></small></td>
    <td width="30%"><small>
       Sophia Laakso,<br>&nbsp;&nbsp;office&nbsp;manager<br>
       voice: +1 503-223-9994<br>
       fax: +1 815-301-3568</small></td>
    <td width="40%"><small>
       administrative email:
         <a href="mailto:office@tug.org">office@tug.org</a>
       <br>web site email:
         <a href="mailto:webmaster@tug.org">webmaster@tug.org</a>
       <br><a href="#help">TeXnical support links above</a>
       <br><a href="https://www.facebook.com/groups/TeXUsersGroup">facebook</a>
           - <a href="https://techhub.social/@TeXUsersGroup">mastodon</a>
           - <a href="https://twitter.com/texusersgroup">twitter</a>
       <td></small>
</tr>
</table>

<hr><small>Many thanks to all the individual and <a
href="/instmem.html">institutional</a> members, as well as our <a
href="/donors/">donors</a>, who keep TUG going.  If you're not already a
member, please consider <a href="/join.html">joining TUG</a> or <a
href="/donate.html">making a donation</a>, and
thanks.</small>

<hr><small>Updated: $Date: 2026/09/01 20:49:07 $</small>
</body></html>
```

---

### A.2. Запит без захисту з'єднання

**Команда:**

```
curl -v http://neverssl.com
```

**Вивід:**

```
  % Total    % Received % Xferd  Average Speed  Time    Time    Time   Current
                                 Dload  Upload  Total   Spent   Left   Speed
  0      0   0      0   0      0      0      0                              0* Host neverssl.com:80 was resolved.
* IPv6: 2600:1f13:37c:1400:ba21:7165:5fc7:736e
* IPv4: 34.223.124.45
*   Trying [2600:1f13:37c:1400:ba21:7165:5fc7:736e]:80...
* Immediate connect fail for 2600:1f13:37c:1400:ba21:7165:5fc7:736e: Не вдалося отримати доступ до мережі
*   Trying 34.223.124.45:80...
  0      0   0      0   0      0      0      0           00:05              0* Established connection to neverssl.com (34.223.124.45 port 80) from 192.168.10.152 port 60760 
* using HTTP/1.x
> GET / HTTP/1.1
> Host: neverssl.com
> User-Agent: curl/8.18.0
> Accept: */*
> 
* Request completely sent off
  0      0   0      0   0      0      0      0           00:06              0< HTTP/1.1 200 OK
< Date: Wed, 09 Sep 2026 08:23:07 GMT
< Server: Apache/2.4.66 ()
< Upgrade: h2,h2c
< Connection: Upgrade
< Last-Modified: Wed, 29 Jun 2022 00:23:33 GMT
< ETag: "f79-5e28b29d38e93"
< Accept-Ranges: bytes
< Content-Length: 3961
< Vary: Accept-Encoding
< Content-Type: text/html; charset=UTF-8
< 
{ [3961 bytes data]
100   3961 100   3961   0      0    595      0   00:06   00:06            704
* Connection #0 to host neverssl.com:80 left intact
<html>
	<head>
		<title>NeverSSL - Connecting ... </title>
		<style>
		body {
			font-family: Montserrat, helvetica, arial, sans-serif;
			font-size: 16x;
			color: #444444;
			margin: 0;
		}
		h2 {
			font-weight: 700;
			font-size: 1.6em;
			margin-top: 30px;
		}
		p {
			line-height: 1.6em;
		}
		.container {
			max-width: 650px;
			margin: 20px auto 20px auto;
			padding-left: 15px;
			padding-right: 15px
		}
		.header {
			background-color: #42C0FD;
			color: #FFFFFF;
			padding: 10px 0 10px 0;
			font-size: 2.2em;
		}
		.notice {
			background-color: red;
			color: white;
			padding: 10px 0 10px 0;
			font-size: 1.25em;
			animation: flash 4s infinite;
		}
		@keyframes flash {
		0% {
			background-color: red;
		}
		50% {
			background-color: #AA0000;
		}
		0% {
			background-color: red;
		}
		}
		<!-- CSS from Mark Webster https://gist.github.com/markcwebster/9bdf30655cdd5279bad13993ac87c85d -->
		</style>

		<script>
			var adjectives = [ 'cool' , 'calm' , 'relaxed', 'soothing', 'serene', 'slow',
							'beautiful', 'wonderful', 'wonderous', 'fun', 'good',
							'glowing', 'inner', 'grand', 'majestic', 'astounding',
							'fine', 'splendid', 'transcendent', 'sublime', 'whole',
							'unique', 'old', 'young', 'fresh', 'clear', 'shiny',
							'shining', 'lush', 'quiet', 'bright', 'silver' ];

			var nouns =	  [ 'day', 'dawn', 'peace', 'smile', 'love', 'zen', 'laugh',
							'yawn', 'poem', 'song', 'joke', 'verse', 'kiss', 'sunrise',
							'sunset', 'eclipse', 'moon', 'rainbow', 'rain', 'plan',
							'play', 'chart', 'birds', 'stars', 'pathway', 'secret',
							'treasure', 'melody', 'magic', 'spell', 'light', 'morning'];

			var prefix =
					// Choose 3 zen adjectives
					adjectives.sort(function(){return 0.5-Math.random()}).slice(-3).join('')
					+
					// Coupled with a zen noun
					nouns.sort(function(){return 0.5-Math.random()}).slice(-1).join('');
			window.location.href = 'http://' + prefix + '.neverssl.com/online';
		</script>
	</head>
	<body>
	<noscript>
		<div class="notice">
			<div class="container">
				⚠️ JavaScript appears to be disabled. NeverSSL's cache-busting works better if you enable JavaScript for <code>neverssl.com</code>.
			</div>
		</div>
	</noscript>
	<div class="header">
		<div class="container">
		<h1>NeverSSL</h1>
		</div>
	</div>
	<div class="content">
	<div class="container">

	<h1 id="status"></h1>
	<script>document.querySelector("#status").textContent = "Connecting ...";</script>
	<noscript>

		<h2>What?</h2>
		<p>This website is for when you try to open Facebook, Google, Amazon, etc
		on a wifi network, and nothing happens. Type "http://neverssl.com"
		into your browser's url bar, and you'll be able to log on.</p>

		<h2>How?</h2>
		<p>neverssl.com will never use SSL (also known as TLS). No
		encryption, no strong authentication, no <a
		href="https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security">HSTS</a>,
		no HTTP/2.0, just plain old unencrypted HTTP and forever stuck in the dark
		ages of internet security.</p>

		<h2>Why?</h2>
		<p>Normally, that's a bad idea. You should always use SSL and secure
		encryption when possible. In fact, it's such a bad idea that most websites
		are now using https by default.</p>

		<p>And that's great, but it also means that if you're relying on
		poorly-behaved wifi networks, it can be hard to get online.  Secure
		browsers and websites using https make it impossible for those wifi
		networks to send you to a login or payment page. Basically, those networks
		can't tap into your connection just like attackers can't. Modern browsers
		are so good that they can remember when a website supports encryption and
		even if you type in the website name, they'll use https.</p>

		<p>And if the network never redirects you to this page, well as you can
		see, you're not missing much.</p>

        <a href="https://twitter.com/neverssl">Follow @neverssl</a>

	</noscript>

	</div>
	</div>

	</body>
</html>
```

---

### A.3. Запит до служби доменних імен

**Команда (перше виконання):**

```
dig tug.org
```

**Вивід:**

```
; <<>> DiG 9.20.24-1ubuntu0.3-Ubuntu <<>> tug.org
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 39717
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;tug.org.			IN	A

;; ANSWER SECTION:
tug.org.		5531	IN	A	46.4.94.215

;; Query time: 0 msec
;; SERVER: 127.0.0.53#53(127.0.0.53) (UDP)
;; WHEN: Wed Sep 09 11:31:23 EEST 2026
;; MSG SIZE  rcvd: 52

```

**Команда (повторне виконання через 5–7 хвилин):**

```
dig tug.org
```

**Вивід:**

```
; <<>> DiG 9.20.24-1ubuntu0.3-Ubuntu <<>> tug.org
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 28722
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;tug.org.			IN	A

;; ANSWER SECTION:
tug.org.		5158	IN	A	46.4.94.215

;; Query time: 0 msec
;; SERVER: 127.0.0.53#53(127.0.0.53) (UDP)
;; WHEN: Wed Sep 09 11:37:36 EEST 2026
;; MSG SIZE  rcvd: 52

```

**Зафіксовані значення:**

| Параметр | Перше виконання | Повторне виконання |
|---|---|---|
| Час виконання (год:хв) | 11:31 | 11:37 |
| IP-адреса | 46.4.94.215 | 46.4.94.215 |
| Значення TTL | 5531 | 5158 |

> Якщо друге значення TTL виявилося більшим за перше — це нормально: кеш резолвера встиг оновитися. Зафіксуйте як є.

---

### A.4. Контрольний ресурс

**Команда:**

```
curl -v https://google.com
```

**Вивід:**

```
  % Total    % Received % Xferd  Average Speed  Time    Time    Time   Current
                                 Dload  Upload  Total   Spent   Left   Speed
  0      0   0      0   0      0      0      0                              0* Host google.com:443 was resolved.
* IPv6: 2a00:1450:400d:802::200e
* IPv4: 142.251.140.78
*   Trying [2a00:1450:400d:802::200e]:443...
* Immediate connect fail for 2a00:1450:400d:802::200e: Не вдалося отримати доступ до мережі
*   Trying 142.251.140.78:443...
* ALPN: curl offers h2,http/1.1
} [5 bytes data]
* TLSv1.3 (OUT), TLS handshake, Client hello (1):
} [1565 bytes data]
* SSL Trust Anchors:
*   CAfile: /etc/ssl/certs/ca-certificates.crt
*   CApath: /etc/ssl/certs
{ [5 bytes data]
* TLSv1.3 (IN), TLS handshake, Server hello (2):
{ [1210 bytes data]
* TLSv1.3 (IN), TLS change cipher, Change cipher spec (1):
{ [1 bytes data]
* TLSv1.3 (IN), TLS handshake, Encrypted Extensions (8):
{ [15 bytes data]
* TLSv1.3 (IN), TLS handshake, Certificate (11):
{ [4835 bytes data]
* TLSv1.3 (IN), TLS handshake, CERT verify (15):
{ [79 bytes data]
* TLSv1.3 (IN), TLS handshake, Finished (20):
{ [52 bytes data]
* TLSv1.3 (OUT), TLS change cipher, Change cipher spec (1):
} [1 bytes data]
* TLSv1.3 (OUT), TLS handshake, Finished (20):
} [52 bytes data]
* SSL connection using TLSv1.3 / TLS_AES_256_GCM_SHA384 / X25519MLKEM768 / id-ecPublicKey
* ALPN: server accepted h2
* Server certificate:
*   subject: CN=*.google.com
*   start date: Sep  4 08:04:41 2026 GMT
*   expire date: Nov 27 08:04:40 2026 GMT
*   issuer: C=US; O=Google Trust Services; CN=WR2
*   Certificate level 0: Public key type EC/prime256v1 (256/128 Bits/secBits), signed using sha256WithRSAEncryption
*   Certificate level 1: Public key type RSA (2048/112 Bits/secBits), signed using sha256WithRSAEncryption
*   Certificate level 2: Public key type RSA (4096/152 Bits/secBits), signed using sha384WithRSAEncryption
*   subjectAltName: "google.com" matches cert's "google.com"
* SSL certificate verified via OpenSSL.
* Established connection to google.com (142.251.140.78 port 443) from 192.168.10.152 port 60532 
* using HTTP/2
* [HTTP/2] [1] OPENED stream for https://google.com/
* [HTTP/2] [1] [:method: GET]
* [HTTP/2] [1] [:scheme: https]
* [HTTP/2] [1] [:authority: google.com]
* [HTTP/2] [1] [:path: /]
* [HTTP/2] [1] [user-agent: curl/8.18.0]
* [HTTP/2] [1] [accept: */*]
} [5 bytes data]
> GET / HTTP/2
> Host: google.com
> User-Agent: curl/8.18.0
> Accept: */*
> 
* Request completely sent off
} [5 bytes data]
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
{ [283 bytes data]
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
{ [283 bytes data]
< HTTP/2 301 
< location: https://www.google.com/
< content-type: text/html; charset=UTF-8
< content-security-policy-report-only: object-src 'none';base-uri 'self';script-src 'nonce-4eJGc5TFQDXZSwd9dBVvTw' 'strict-dynamic' 'report-sample' 'unsafe-eval' 'unsafe-inline' https: http:;report-uri https://csp.withgoogle.com/csp/gws/other-hp
< date: Sun, 20 Sep 2026 13:13:12 GMT
< expires: Tue, 20 Oct 2026 13:13:12 GMT
< cache-control: public, max-age=2592000
< server: gws
< content-length: 220
< x-xss-protection: 0
< x-frame-options: SAMEORIGIN
< alt-svc: h3=":443"; ma=2592000,h3-29=":443"; ma=2592000
< 
{ [5 bytes data]
100    220 100    220   0      0    585      0                              0
* Connection #0 to host google.com:443 left intact
<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="https://www.google.com/">here</A>.
</BODY></HTML>
```

---

### A.5. Ресурси з некоректною конфігурацією сертифіката

**Випадок 1**

```
curl -v https://expired.badssl.com
```

```
% Total    % Received % Xferd  Average Speed  Time    Time    Time   Current
                                 Dload  Upload  Total   Spent   Left   Speed
  0      0   0      0   0      0      0      0                              0* Host expired.badssl.com:443 was resolved.
* IPv6: (none)
* IPv4: 104.154.89.105
*   Trying 104.154.89.105:443...
* ALPN: curl offers h2,http/1.1
} [5 bytes data]
* TLSv1.3 (OUT), TLS handshake, Client hello (1):
} [1573 bytes data]
* SSL Trust Anchors:
*   CAfile: /etc/ssl/certs/ca-certificates.crt
*   CApath: /etc/ssl/certs
{ [5 bytes data]
* TLSv1.3 (IN), TLS handshake, Server hello (2):
{ [108 bytes data]
* TLSv1.2 (IN), TLS handshake, Certificate (11):
{ [4323 bytes data]
* TLSv1.2 (IN), TLS handshake, Server key exchange (12):
{ [333 bytes data]
* TLSv1.2 (IN), TLS handshake, Server finished (14):
{ [4 bytes data]
* TLSv1.2 (OUT), TLS handshake, Client key exchange (16):
} [70 bytes data]
* TLSv1.2 (OUT), TLS change cipher, Change cipher spec (1):
} [1 bytes data]
* TLSv1.2 (OUT), TLS handshake, Finished (20):
} [16 bytes data]
* TLSv1.2 (IN), TLS handshake, Finished (20):
{ [16 bytes data]
* SSL connection using TLSv1.2 / ECDHE-RSA-AES128-GCM-SHA256 / secp256r1 / rsaEncryption
* ALPN: server accepted http/1.1
* Server certificate:
*   subject: OU=Domain Control Validated; OU=PositiveSSL Wildcard; CN=*.badssl.com
*   start date: Apr  9 00:00:00 2015 GMT
*   expire date: Apr 12 23:59:59 2015 GMT
*   issuer: C=GB; ST=Greater Manchester; L=Salford; O=COMODO CA Limited; CN=COMODO RSA Domain Validation Secure Server CA
*   Certificate level 0: Public key type RSA (2048/112 Bits/secBits), signed using sha256WithRSAEncryption
*   Certificate level 1: Public key type RSA (2048/112 Bits/secBits), signed using sha384WithRSAEncryption
*   Certificate level 2: Public key type RSA (4096/152 Bits/secBits), signed using sha384WithRSAEncryption
*   subjectAltName: "expired.badssl.com" matches cert's "*.badssl.com"
* SSL certificate OpenSSL verify result: certificate has expired (10)

* closing connection #0
curl: (60) SSL certificate OpenSSL verify result: certificate has expired (10)
More details here: https://curl.se/docs/sslcerts.html

curl failed to verify the legitimacy of the server and therefore could not
establish a secure connection to it. To learn more about this situation and
how to fix it, please visit the webpage mentioned above.

```

**Випадок 2**

```
curl -v https://wrong.host.badssl.com
```

```
  % Total    % Received % Xferd  Average Speed  Time    Time    Time   Current
                                 Dload  Upload  Total   Spent   Left   Speed
  0      0   0      0   0      0      0      0                              0* Host wrong.host.badssl.com:443 was resolved.
* IPv6: (none)
* IPv4: 104.154.89.105
*   Trying 104.154.89.105:443...
* ALPN: curl offers h2,http/1.1
} [5 bytes data]
* TLSv1.3 (OUT), TLS handshake, Client hello (1):
} [1576 bytes data]
* SSL Trust Anchors:
*   CAfile: /etc/ssl/certs/ca-certificates.crt
*   CApath: /etc/ssl/certs
{ [5 bytes data]
* TLSv1.3 (IN), TLS handshake, Server hello (2):
{ [108 bytes data]
* TLSv1.2 (IN), TLS handshake, Certificate (11):
{ [4074 bytes data]
* TLSv1.2 (IN), TLS handshake, Server key exchange (12):
{ [333 bytes data]
* TLSv1.2 (IN), TLS handshake, Server finished (14):
{ [4 bytes data]
* TLSv1.2 (OUT), TLS handshake, Client key exchange (16):
} [70 bytes data]
* TLSv1.2 (OUT), TLS change cipher, Change cipher spec (1):
} [1 bytes data]
* TLSv1.2 (OUT), TLS handshake, Finished (20):
} [16 bytes data]
* TLSv1.2 (IN), TLS handshake, Finished (20):
{ [16 bytes data]
* SSL connection using TLSv1.2 / ECDHE-RSA-AES128-GCM-SHA256 / secp256r1 / rsaEncryption
* ALPN: server accepted http/1.1
* Server certificate:
*   subject: CN=*.badssl.com
*   start date: Jul 28 20:03:02 2026 GMT
*   expire date: Oct 26 20:03:01 2026 GMT
*   issuer: C=US; O=Let's Encrypt; CN=YR2
*   Certificate level 0: Public key type RSA (2048/112 Bits/secBits), signed using sha256WithRSAEncryption
*   Certificate level 1: Public key type RSA (2048/112 Bits/secBits), signed using sha256WithRSAEncryption
*   Certificate level 2: Public key type RSA (4096/152 Bits/secBits), signed using sha256WithRSAEncryption
*   Certificate level 3: Public key type RSA (4096/152 Bits/secBits), signed using sha256WithRSAEncryption
*  subjectAltName does not match hostname wrong.host.badssl.com
* SSL: no alternative certificate subject name matches target hostname 'wrong.host.badssl.com'

* closing connection #0
curl: (60) SSL: no alternative certificate subject name matches target hostname 'wrong.host.badssl.com'
More details here: https://curl.se/docs/sslcerts.html

curl failed to verify the legitimacy of the server and therefore could not
establish a secure connection to it. To learn more about this situation and
how to fix it, please visit the webpage mentioned above.

```

**Випадок 3**

```
curl -v https://self-signed.badssl.com
```

```
  % Total    % Received % Xferd  Average Speed  Time    Time    Time   Current
                                 Dload  Upload  Total   Spent   Left   Speed
  0      0   0      0   0      0      0      0                              0* Host self-signed.badssl.com:443 was resolved.
* IPv6: (none)
* IPv4: 104.154.89.105
*   Trying 104.154.89.105:443...
* ALPN: curl offers h2,http/1.1
} [5 bytes data]
* TLSv1.3 (OUT), TLS handshake, Client hello (1):
} [1577 bytes data]
* SSL Trust Anchors:
*   CAfile: /etc/ssl/certs/ca-certificates.crt
*   CApath: /etc/ssl/certs
{ [5 bytes data]
* TLSv1.3 (IN), TLS handshake, Server hello (2):
{ [108 bytes data]
* TLSv1.2 (IN), TLS handshake, Certificate (11):
{ [903 bytes data]
* TLSv1.2 (IN), TLS handshake, Server key exchange (12):
{ [333 bytes data]
* TLSv1.2 (IN), TLS handshake, Server finished (14):
{ [4 bytes data]
* TLSv1.2 (OUT), TLS handshake, Client key exchange (16):
} [70 bytes data]
* TLSv1.2 (OUT), TLS change cipher, Change cipher spec (1):
} [1 bytes data]
* TLSv1.2 (OUT), TLS handshake, Finished (20):
} [16 bytes data]
* TLSv1.2 (IN), TLS handshake, Finished (20):
{ [16 bytes data]
* SSL connection using TLSv1.2 / ECDHE-RSA-AES128-GCM-SHA256 / secp256r1 / rsaEncryption
* ALPN: server accepted http/1.1
* Server certificate:
*   subject: C=US; ST=California; L=San Francisco; O=BadSSL; CN=*.badssl.com
*   start date: Sep 15 21:01:28 2026 GMT
*   expire date: Sep 14 21:01:28 2028 GMT
*   issuer: C=US; ST=California; L=San Francisco; O=BadSSL; CN=*.badssl.com
*   Certificate level 0: Public key type RSA (2048/112 Bits/secBits), signed using sha256WithRSAEncryption
*   subjectAltName: "self-signed.badssl.com" matches cert's "*.badssl.com"
* SSL certificate OpenSSL verify result: self-signed certificate (18)

* closing connection #0
curl: (60) SSL certificate OpenSSL verify result: self-signed certificate (18)
More details here: https://curl.se/docs/sslcerts.html

curl failed to verify the legitimacy of the server and therefore could not
establish a secure connection to it. To learn more about this situation and
how to fix it, please visit the webpage mentioned above.

```
---

## Частина B. Власна модель рівнів

**Кількість виділених груп:** 4

| № | Назва групи (власне формулювання) | Рядки виводу, віднесені до групи | Обґрунтування |
|---|---|---|---|
| 1 | Запит і відповідь | усі рядки з > та <, разом із тілом від <!DOCTYPE html> до </body></html> | Рівень спілкування програми із сервером: запит і відповідь.Текст HTML сюди ж, бо це просто результат цього запиту |
| 2 | Чи це справді той сервер | від `* ALPN: curl offers h2,http/1.1` до `* SSL certificate verified via OpenSSL` | Тут клієнт перевіряє сертифікат і домовляється про шифрування |
| 3 | Підключення до сервера | `*   Trying 46.4.94.215:443...`, `* Established connection to tug.org (46.4.94.215 port 443) from 192.168.10.152 port 34660` | Звичайне підключення, коли зв'язок уже з'явився, але обмін даними ще не почався |
| 4 | Пошук адреси за іменем | `* Host tug.org:443 was resolved.`, `* IPv6: (none)`, `* IPv4: 46.4.94.215` | Пошук адреси сайту за його назвою. Це підготовчий крок, бо комп'ютер не знає куди звертатися, поки не отримає цифри замість імені |

*Групи впорядковано від найближчої до користувача (№ 1) до найближчої до апаратного забезпечення. Зайві рядки вилучити, за потреби — додати.*

**Рядки, які не вдалося віднести до жодної групи:**

| Рядок виводу | Причина утруднення |
|---|---|
| % Total    % Received % Xferd  Average Speed |  Індикатор прогресу самої утиліти, який не стосується мережі та вивівся суто через запис у файлі |
| } [5 bytes data] / { [1562 bytes data] | Зашифровані дані без відкритого тексту, які трапляються одночасно і в TLS, і в HTTP |
| * Request completely sent off | Службове повідомлення самої програми про стан відправки, яке опинилося прямо між групами |

---

## Контрольні питання

**1. Скільки рядків діагностичного виводу передує отриманню даних сторінки (завдання A.1)?**

> Перші 67 рядків займає діагностика curl і заголовки, а сама сторінка починається з 68 рядка

**2. Які рядки наявні у виводі A.1 і відсутні у виводі A.2? Чим це зумовлено?**

> В A.1 є налаштування шифрування, а в A.2 його немає, бо там простий HTTP без захисту

**3. Звідки у виводі з'явилося значення `443`, якщо його не було вказано в адресі?**

> Порт 443 вибрався сам, бо це стандарт для HTTPS

**4. Як змінилося значення TTL між двома запитами (A.3)? Що означає це число?**

> TTL зменшився рівно на 373 секунди, бо саме стільки часу пройшло між двома запитами. Це звичайний таймер, який показує скільки секунд запис ще проживе в кеші

**5. Чим відрізняються між собою три причини помилок із завдання A.5? Сформулювати кожну однією фразою.**

| Випадок | Причина недовіри |
|---|---|
| `expired` | Сертифікат прострочений, бо його термін дії закінчився ще у 2015 році |
| `wrong.host` | Адреса сайту не збігається з іменем, яке вказане в сертифікаті |
| `self-signed` | Сервер сам собі підписав сертифікат замість офіційного центру сертифікації |

**6. Три рядки з власних виводів, про які не йшлося на лекції 1:**

| № | Рядок виводу | Джерело (номер завдання) |
|---|---|---|
| 1 | * ALPN: curl offers h2,http/1.1 | а.1 |
| 2 | * Immediate connect fail for 2600:1f13:37c:1400:ba21:7165:5fc7:736e: Не вдалося отримати доступ до мережі | а.2 |
| 3 | EDNS: version: 0, flags:; udp: 65494 | а.3 |

---

## Висновки

*150–300 слів. Спиратися на власні спостереження, а не на матеріал лекції.*

**D.1. Що виявилося неочевидним або несподіваним**

*Назвати конкретно, з посиланням на рядок виводу.*

> Не знав, що довіра до сайтів перевіряється через стандартний список сертифікатів, який уже був встановлений у моїй системі. У виводі це видно в рядку `CAfile: /etc/ssl/certs/ca-certificates.crt`

**D.2. Чому саме така кількість груп у частині B**

*На якій підставі ухвалено рішення. Що змусило б його змінити.*

> Виділив 4 групи тільки за тими кроками, які реально є у виводі. Змінив би поділ і додав нові рівні, якби в терміналі з'явилися дані про маршрутизацію чи MAC-адреси

**D.3. Питання, яке залишилося без відповіді**

> Чому сервер заявляє підтримку HTTP/2 через Upgrade: h2, але в ALPN обирає старіший http/1.1? Не зрозумів, від чого залежить цей вибір

---

## Використання штучного інтелекту

*Розділ обов'язковий. Заповнюється незалежно від того, чи використовувався ШІ. Детальні вимоги — у документі «Політика використання технологій штучного інтелекту».*

**Факт використання:** використано *(потрібне залишити)*

**Установлений рівень для цієї роботи:** Р3 — ШІ як співвиконавець

**Фактичний рівень використання:** Р1

### Використані системи

| Система | Версія або модель | Період використання |
|---|---|---|
| | | |

### Промпти

*Наводити дослівно, у тому вигляді, у якому запит було надано системі. Переказ не приймається.*

| № | Розділ роботи | Текст промпта |
|---|---|---|
| 1 | | |
| 2 | | |
| 3 | | |

### Дії з отриманим результатом

| № промпта | Що перевірено | Що змінено | Що відхилено і чому |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

### Підтвердження

Підтверджую, що всі наведені в цьому звіті виводи команд отримано мною особисто внаслідок фактичного виконання відповідних дій, а відомості цього розділу є повними та достовірними.

> Виводи `curl`, `dig` та інші артефакти не можуть бути згенеровані. Це стосується будь-якого рівня використання ШІ.

---

## Примітки виконавця

*(необов'язковий розділ: що не спрацювало, які команди довелося змінити, які виникли труднощі)*
