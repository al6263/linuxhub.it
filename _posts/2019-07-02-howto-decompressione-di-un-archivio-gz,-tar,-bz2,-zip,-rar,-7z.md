---
title: '#howto - Decompressione di un archivio (gz, tar, bz2, zip, rar, 7z)'
published: 2019-07-02
layout: post
author: Mirko B.
author_github: mirkobrombin
tags:
  - bash
---
<p>I formati di compressione sono molti e spesso sono altrettanto differenti gli strumenti per decomprimerli.</p><p>In questa guida vediamo come decomprimere i principali formati di compressione.</p><h2>Gz</h2><p>Per decomprimere un archivio in <strong>.gz</strong>, possiamo usare il comando <strong>gunzip</strong>:</p><pre><code>gunzip archivio.gz</code></pre><p>in alternativa possiamo usare il comando <strong>gzip</strong> con la flag <strong>-d</strong>:</p><pre><code>gzip -d archivio.gz</code></pre><h2>Bzip2</h2><p>Possiamo decomprimere un archivio in formato <strong>.bzip2</strong>, tramite l'omonimo strumento e la flag <strong>-d</strong>:</p><pre><code>bzip2 -d archivio.bzip</code></pre><p>in alternativa <strong>bunzip2</strong>:</p><pre><code>bunzip2 archivio.bzip2</code></pre><h2>Zip</h2><p>Forse il formato di compressione più comune, può essere decompresso mediante comando <strong>unzip</strong> (spesso non pre-installato nel sistema):</p><pre><code>unzip archivio.zip</code></pre><p>Possiamo installarlo mediante gestore pacchetti di sistema:</p><pre><code># Debian/Ubuntu e derivateapt install unzip# RHEL/Centos e derivateyum install unzip# Fedora e derivatednf install unzip# Arch Linux e derivatepacman -S unzip</code></pre><h2>Tar</h2><p>Per decomprimere un archivio <strong>.tar</strong>, possiamo sfruttare l'omonimo comando con l'opzione <strong>xf</strong> come segue:</p><pre><code>tar xf archivio.tar</code></pre><p>Esistono poi altre tipologie di archivi .tar che sfruttano una compressione differente, come ad esempio <strong>bzip2</strong> o <strong>gzip</strong>.</p><h3>Tar.gz</h3><p>Per decomprimere un archivio <strong>.tar</strong> con compressione <strong>gzip</strong>, possiamo usare l'opzione <strong>xzf</strong>:</p><pre><code>tar xzf archivio.tar.gz</code></pre><h3>Tar.bz2</h3><p>La decompressione di un archivio <strong>.tar</strong> con compressione <strong>bzip2</strong> avviene mediante opzione <strong>xjf</strong>:</p><pre><code>tar xjf archivio.tar.bz</code></pre><h2>Rar</h2><p>Il formato di compressione proprietario <strong>.rar</strong>, richiede l'installazione di uno strumento proprietario per la loro decompressione:</p><pre><code># Debian/Ubuntu e derivateapt install unrar# RHEL/Centos e derivateyum install unrar# Fedora e derivatednf install unrar# Arch Linux e derivatepacman -S unrar</code></pre><p>di norma questo pacchetto viene fornito da repository di software proprietario del sistema o di terze parti.</p><p>Infine possiamo decomprimere un archivio <strong>.rar</strong> mediante l'opzione <strong>x</strong>:</p><pre><code>unrar x archivio.rar</code></pre><h2>7z</h2><p>Come per unrar e unzip, 7z non è sempre offerto come standard in una distribuzione ma possiamo installarlo tramite gestore pacchetti:</p><pre><code class="language-bash"># Debian/Ubuntu e derivateapt install p7zip-full# RHEL/Centos e derivateyum install p7zip p7zip-plugins# Fedora e derivatednf install p7zip p7zip-plugins# Arch Linux e derivatepacman -S p7zip</code></pre><p>e possiamo decomprimere l'archivio come segue:</p><pre><code class="language-bash">7za e archivio.7z</code></pre><p>&nbsp;</p><p><em>Good&nbsp;<strong>*nix</strong>?</em><br /><em>&nbsp;- Mirko</em></p>