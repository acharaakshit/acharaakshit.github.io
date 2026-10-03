---
layout: about
title: home
permalink: /
summary: I study how vision models form, align, and misuse predictive representations, with a focus on failure modes that remain hidden under aggregate performance metrics.

profile:
  image: prof_pic.jpg

news: false
---

<section class="academic-section academic-about" id="research" aria-labelledby="about-heading">
  <div class="academic-section-title">
    <h2 id="about-heading">About</h2>
  </div>
  <div class="academic-section-body academic-prose">
    <p>I am a PhD student at King’s College London, supervised by <a href="https://www.kclmmag.org/team/andrew-king">Prof Andrew King</a>, <a href="https://www.kcl.ac.uk/people/alexander-hammers">Prof Alexander Hammers</a>, and <a href="https://scholar.google.co.uk/citations?user=KbyHPpUAAAAJ&amp;hl=en">Dr Esther Puyol Antón</a>. I am part of the <a href="https://www.drive-health.org.uk/">DRIVE-Health</a> Centre for Doctoral Training and the <a href="https://www.kclmmag.org/home">Motion Modelling &amp; Analysis Group</a>.</p>

    <p class="research-thesis">My research is guided by a central question: <em>does the model rely on evidence that is meaningful, robust, and generalisable?</em></p>

    <ul class="research-questions">
      <li>For image-level and pixel-level classifiers, did the model rely on a spurious or non-generalisable feature? I have studied this through shortcut discovery, spatial localisation, demographic bias, and semantic failures under correlation shift.</li>
      <li>For vision–language models, how do visual and linguistic information interact to shape a prediction? Findings such as <a href="https://arxiv.org/abs/2603.21687">mirage reasoning</a> motivate my interest in auditing multimodal reasoning across conventional VLMs and encoder-free multimodal architectures.</li>
      <li>For medical vision systems, can safety-critical or adversarial visual information bypass a model’s safeguards, and can these failures be detected from its internal representations?</li>
    </ul>

    <p>My current focus is on the latter two questions, which I approach from an interpretability perspective by studying how visual information is encoded and used within model representations, particularly in relation to model safety.</p>

    <p>Before joining King’s, I was a Research Engineer at <a href="https://www.ge.com/">GE Research</a> and <a href="https://www.gehealthcare.com/">GE HealthCare</a>, working on applied machine learning for medical imaging and clinical text. I hold an integrated MSc in Mathematics from <a href="https://www.bits-pilani.ac.in/">BITS Pilani</a>.</p>

  </div>
</section>

<section class="academic-section" id="publications" aria-labelledby="publications-heading">
  <div class="academic-section-title">
    <h2 id="publications-heading">Selected publications</h2>
    <a href="https://scholar.google.com/citations?user=F4uM5vAAAAAJ">Google Scholar</a>
  </div>
  <div class="academic-section-body publication-list">
    <article class="publication-entry">
      <div class="publication-year">2026</div>
      <div>
        <h3>Discovery and Spatial Characterisation of Multiple Shortcut Groups for Auditing Vision Model Bias</h3>
        <p><strong>Akshit Achara</strong>, V. Manickam, T. Day, E. Puyol Anton, A. Hammers, and A. P. King.</p>
        <p class="publication-venue">arXiv, 2026. <span class="publication-links"><a href="https://arxiv.org/pdf/2608.14051">PDF</a></span></p>
      </div>
    </article>

    <article class="publication-entry">
      <div class="publication-year">2026</div>
      <div>
        <h3>EquiSteer: Cross-Attention Steering Towards a Fairer Text-Guided Image Generation</h3>
        <p>T. Gaintseva, <strong>Akshit Achara</strong>, G. Slabaugh, J. Deng, and I. Elezi.</p>
        <p class="publication-venue">ECCV 2026. <span class="publication-links"><a href="https://arxiv.org/pdf/2607.01147">PDF</a></span></p>
      </div>
    </article>

    <article class="publication-entry">
      <div class="publication-year">2026</div>
      <div>
        <h3>Multi-Way Representation Alignment</h3>
        <p><strong>Akshit Achara</strong>, T. Gaintseva, M. Mahaut, P. Chakraborty, V. S. Johansson, M. Barsbey, E. Rodolà, and D. Crisostomi.</p>
        <p class="publication-venue">ICML 2026; ReAlign at ICLR 2026. <span class="publication-links"><a href="https://arxiv.org/pdf/2602.06205">PDF</a></span></p>
      </div>
    </article>

    <article class="publication-entry">
      <div class="publication-year">2026</div>
      <div>
        <h3>Understanding Sources of Demographic Predictability in Brain MRI via Disentangling Anatomy and Contrast</h3>
        <p>M. Y. Avci*, <strong>Akshit Achara*</strong>, A. King, and J. Cardoso, for the Alzheimer’s Disease Neuroimaging Initiative.</p>
        <p class="publication-venue">FAIMI at MICCAI 2026. <span>* Joint first authors; joint supervisors.</span> <span class="publication-links"><a href="https://arxiv.org/pdf/2603.04113">PDF</a></span></p>
      </div>
    </article>

    <article class="publication-entry">
      <div class="publication-year">2026</div>
      <div>
        <h3>Right Regions, Wrong Labels: Semantic Label Flips in Segmentation under Correlation Shift</h3>
        <p><strong>Akshit Achara</strong>, Y. Yathathugoda, N. Byrne, M. Antonelli, E. Puyol Anton, A. Hammers, and A. P. King.</p>
        <p class="publication-venue">Catch, Adapt and Operate (CAO) at ICLR 2026. <span class="publication-links"><a href="https://arxiv.org/pdf/2604.13326">PDF</a></span></p>
      </div>
    </article>

    <article class="publication-entry">
      <div class="publication-year">2025</div>
      <div>
        <h3>Localising Shortcut Learning in Pixel Space via Ordinal Scoring Correlations for Attribution Representations (OSCAR)</h3>
        <p><strong>Akshit Achara</strong>, P. Triantafillou, E. Puyol-Antón, A. Hammers, and A. P. King.</p>
        <p class="publication-venue">arXiv, 2025. <span class="publication-links"><a href="https://arxiv.org/pdf/2512.18888">PDF</a></span></p>
      </div>
    </article>

    <article class="publication-entry">
      <div class="publication-year">2025</div>
      <div>
        <h3>Invisible Attributes, Visible Biases: Exploring Demographic Shortcuts in MRI-based Alzheimer’s Disease Classification</h3>
        <p><strong>Akshit Achara</strong>, E. Puyol Anton, A. Hammers, and A. P. King.</p>
        <p class="publication-venue">FAIMI at MICCAI 2025. <span class="publication-links"><a href="https://arxiv.org/pdf/2509.09558">PDF</a></span></p>
      </div>
    </article>

    <article class="publication-entry">
      <div class="publication-year">2025</div>
      <div>
        <h3>Watching the AI Watchdogs: A Fairness and Robustness Analysis of AI Safety Moderation Classifiers</h3>
        <p><strong>Akshit Achara</strong> and A. Chhabra.</p>
        <p class="publication-venue">NAACL 2025. <span class="publication-links"><a href="https://arxiv.org/pdf/2501.13302">PDF</a></span></p>
      </div>
    </article>

  </div>
</section>
