# Awesome Keystroke Dynamics

A curated list of resources on **keystroke dynamics**, also called typing biometrics or keystroke
biometrics: recognising people by *how* they type rather than *what* they type. It covers
introductions, key papers, public datasets, open-source code and tools.

Keystroke dynamics is a form of behavioural biometrics. Typing rhythm is personal data, and in
the EU it is biometric data under the GDPR (Article 4(14)), so handle any dataset or capture with care.

## Contents

- [Introductions](#introductions)
- [Surveys and reviews](#surveys-and-reviews)
- [Foundational papers](#foundational-papers)
- [Attacks and robustness](#attacks-and-robustness)
- [Deep learning](#deep-learning)
- [Large-scale typing studies](#large-scale-typing-studies)
- [Health](#health)
- [Datasets](#datasets)
- [Open-source code](#open-source-code)
- [Applications and demos](#applications-and-demos)
- [Commercial services](#commercial-services)
- [Contributing](#contributing)

## Introductions

- [Keystroke dynamics: what it is and how it works](https://keybio.pages.dev/en/guides/keystroke-dynamics) - What is measured (dwell time, flight time, n-graphs), verification vs identification, accuracy, uses and privacy.
- [Keystroke dynamics algorithms, explained](https://keybio.pages.dev/en/guides/keystroke-dynamics-algorithms) - Scaled Manhattan distance, Gunetti and Picardi's R and A measures, thresholds, EER and deep learning, with worked examples.
- [Behavioural biometrics: what it is, types and examples](https://keybio.pages.dev/en/guides/behavioral-biometrics) - Keystroke dynamics in the wider context of mouse dynamics, touch gestures, gait and voice.
- [Guías en español](https://keybio.pages.dev/guias/) - The same guides in Spanish (*dinámica de tecleo*, *biometría del comportamiento*).
- [Keystroke dynamics (Wikipedia)](https://en.wikipedia.org/wiki/Keystroke_dynamics) - Overview and history.

## Surveys and reviews

- Teh, Teoh and Yue (2013). [A Survey of Keystroke Dynamics Biometrics](https://doi.org/10.1155/2013/408280). *The Scientific World Journal*. Open access.
- Giot, Dorizzi and Rosenberger (2015). [A review on the public benchmark databases for static keystroke dynamics](https://doi.org/10.1016/j.cose.2015.06.008). *Computers & Security*. Compares the public fixed-text datasets. [Open-access version](https://hal.science/hal-01168513).

## Foundational papers

- Joyce and Gupta (1990). [Identity authentication based on keystroke latencies](https://doi.org/10.1145/75577.75582). *Communications of the ACM*. Keystroke latencies as a way to harden password logins.
- Monrose and Rubin (2000). [Keystroke dynamics as a biometric for authentication](https://doi.org/10.1016/S0167-739X(99)00059-X). *Future Generation Computer Systems*.
- Gunetti and Picardi (2005). [Keystroke analysis of free text](https://doi.org/10.1145/1085126.1085129). *ACM Transactions on Information and System Security*. The R (relative order) and A (absolute duration) measures for free text.
- Killourhy and Maxion (2009). [Comparing anomaly-detection algorithms for keystroke dynamics](https://doi.org/10.1109/DSN.2009.5270346). *IEEE/IFIP DSN*. The CMU benchmark: 14 detectors on one shared dataset; scaled Manhattan came out best.

## Attacks and robustness

- Tey, Gupta and Gao (2013). [I can be You: Questioning the use of Keystroke Dynamics as Biometrics](https://www.ndss-symposium.org/ndss2013/i-can-be-you-questioning-use-keystroke-dynamics-biometrics). *NDSS*. Trained imitators with software feedback.
- Serwadda and Phoha (2013). [Examining a Large Keystroke Biometrics Dataset for Statistical-Attack Openings](https://doi.org/10.1145/2516960). *ACM Transactions on Information and System Security*.

## Deep learning

- Acien, Morales, Monaco, Vera-Rodriguez and Fierrez (2022). [TypeNet: Deep Learning Keystroke Biometrics](https://doi.org/10.1109/TBIOM.2021.3112540). *IEEE Transactions on Biometrics, Behavior, and Identity Science*. Recurrent network trained on the Aalto datasets that scales to hundreds of thousands of users. [arXiv](https://arxiv.org/abs/2101.05570).

## Large-scale typing studies

- Dhakal, Feit, Kristensson and Oulasvirta (2018). [Observations on Typing from 136 Million Keystrokes](https://doi.org/10.1145/3173574.3174220). *CHI*. About 168,000 volunteers on physical keyboards.
- Palin, Feit, Kim, Kristensson and Oulasvirta (2019). [How do People Type on Mobile Devices? Observations from a Study with 37,000 Volunteers](https://doi.org/10.1145/3338286.3340120). *MobileHCI*.

## Health

- Giancardo et al. (2016). [Computer keyboard interaction as an indicator of early Parkinson's disease](https://doi.org/10.1038/srep34468). *Scientific Reports*. Hold-time patterns from everyday typing.

## Datasets

- [CMU Keystroke Dynamics Benchmark Data Set](https://www.cs.cmu.edu/~keystroke/) - 51 subjects typing the password `.tie5Roanl` 400 times over 8 sessions (fixed text).
- [Aalto 136M Keystrokes](https://userinterfaces.aalto.fi/136Mkeystrokes/) - Keystroke timings from about 168,000 people typing sentences on physical keyboards.
- [Aalto Mobile Typing](https://userinterfaces.aalto.fi/typing37k/) - Typing data from over 37,000 people on mobile devices.
- [Human-written and synthesized free-text keystroke samples](https://data.mendeley.com/datasets/mzm86rcxxd) - For evaluating liveness detection (telling people from scripts).
- More fixed-text datasets (GREYC, WEBGREYC and others) are compared in Giot et al. (2015), listed above.

## Open-source code

- [njanakiev/keystroke-biometrics](https://github.com/njanakiev/keystroke-biometrics) - Notebooks with scikit-learn and Keras classifiers.
- [gitanat/keystroke_dynamics](https://github.com/gitanat/keystroke_dynamics) - Python identification and authentication from key timings.
- [vikasdesai/keystroke-dynamics](https://github.com/vikasdesai/keystroke-dynamics) - Browser demo of keystroke biometrics.
- [johwconst/keystrokeDynamics2FA](https://github.com/johwconst/keystrokeDynamics2FA) - Keystroke dynamics as a second authentication factor.
- [nileshprasad137/keystroke-dynamics-datagen](https://github.com/nileshprasad137/keystroke-dynamics-datagen) - Generator for keystroke timing datasets.
- [abdullah-arif-swe/KeystrokeDynamicsSpoofer](https://github.com/abdullah-arif-swe/KeystrokeDynamicsSpoofer) - Spoofer for testing how robust keystroke systems are.

## Applications and demos

- [KeyBio](https://keybio.pages.dev/en/) - Free desktop app for Windows, macOS and Linux: free-text identification (1:N), verification (1:1), login checks and PDF reports, with everything stored locally. The website has an in-browser demo that never sends keystrokes. *(Maintained by the author of this list.)*

## Commercial services

- [TypingDNA](https://www.typingdna.com/) - Typing biometrics API for authentication.
- [BioCatch](https://www.biocatch.com/) - Behavioural biometrics for fraud detection in banking.

## Contributing

Contributions are welcome: open a pull request that adds one resource per line, in the right
section, as `[Name](link) - Short description.` Prefer stable links (DOIs, official pages) and
open-access versions where they exist.

## License

[CC0 1.0](LICENSE): to the extent possible under law, the authors have waived all copyright and
related rights to this list.
