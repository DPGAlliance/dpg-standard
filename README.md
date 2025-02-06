[![CC BY-SA 4.0][cc-by-sa-shield]](LICENSE)
[![Contributor Covenant][code-of-conduct-shield]](CODE_OF_CONDUCT.md)

<a href="https://open-stand.org"><img alt="OpenStand Group Logo" height="64px" width="64px" src="https://open-stand.org/wp-content/uploads/2012/08/128x128-green1.png"> </a><br />

<p align="center">
    <img alt="oss image" src="docs/standard-badge.svg" height="150px" width="150px">
</p>
<h1 align="center">Digital Public Goods Standard</h1>

The [Digital Public Goods Standard](standard.md) is a set of specifications and guidelines designed to maximize consensus about whether a project conforms to the definition of digital public goods set by the UN Secretary-General in the [2020 Roadmap for Digital Cooperation](https://www.un.org/en/content/digital-cooperation-roadmap/): *digital public goods must be open source software, open data, open AI models, open standards, and open content that adhere to privacy and other applicable laws and best practices, do no harm, and help attain the Sustainable Development Goals (SDGs).*

The DPG Standard establishes a baseline that must be met in order to earn recognition as a digital public good by the [Digital Public Goods Alliance](https://digitalpublicgoods.net) (DPGA) and the broader community. The DPG Standard is an open project and therefore [open to contribution](standard.md). The DPGA supports the [5 Core Principles of OpenStand](openstand.md) in the development of the DPG Standard.

## 🔎 Current Version

[The DPG Standard](standard.md) is currently at version 1.1.6, published on Sep. 4, 2024; view the [changelog](https://github.com/DPGAlliance/DPG-Standard/blob/master/CHANGELOG.md).

## ✅ Application of the DPG Standard

We encourage creators, maintainers, funders, implementers, and consumers to use this standard to recognize, assess, and support digital public goods. The standard is operationalized through a [questionary](https://app.digitalpublicgoods.net/form) that is required as part of the assessment process. We maintain a list of digital public goods that meet the DPG Standard described above on [our registry](https://digitalpublicgoods.net/registry). Projects are reviewed annually and archived if they do not continue to meet the Standard, as per our [review policy](https://github.com/DPGAlliance/dpg-resources/blob/main/docs/dpg-review-policy.md).

```mermaid
flowchart LR
    A(Submit Application)
    B(L1 Review)
    A --> B
    B --> C(L2 Review)
    C --> D(Waiting for Consultation &lpar;Expert Reviewer&rpar;)
    D --> C
    C --> F{Decision}
    C --> E(Waiting for Clarifications &lpar;Applicant&rpar;)
    E --> A
    F -->|Yes| G(DPG)
    F -->|No| H(Inelligible)
    classDef default font-variant:small-caps,font-family:courier,stroke:#333,color:#000;
    style A fill:#FBF7EF;
    style B fill:#FAC610;
    style C fill:#FAC610;
    style D fill:#FE7F80;
    style E fill:#12CDD4;
    style F fill:#E6E6E6;
    style G fill:#8ED14F;
    style H fill:#F24726;
  
```

We apply the DPG Standard to projects that have been [nominated directly](https://app.digitalpublicgoods.net/form). Solutions submitted to our platform will undergo two stages of review to ensure they meet the requirements set in the DPG Standard. As a project undergoes various reviews it will move from **nominee** to a fully reviewed **digital public good**. If a project meets the DPG Standard it will be officially considered a digital public good and will appear as such in the DPG Registry, and may be eligible for additional recognition and support.

## 🤗 Code of Conduct

The DPGA is dedicated to building a welcoming, diverse, and safe community. We expect everyone participating in the DPGA community to abide by our [**Code of Conduct**](CODE_OF_CONDUCT.md). Please read it. Please follow it. In the DPGA, we work hard to build each other up and create amazing things together. 💪💜

## ⚖️ Governance

At the DPGA, we envision a growing community of contributors and stakeholders around the DPG Standard in an open, transparent, and accessible manner. Our [governance](governance.md) documents the processes for welcoming, reviewing, and merging proposals for modifications to the DPG Standard and manages clear expectations around these processes.

## 🙏 Acknowledgements

Thank you to all the individuals who contributed to the DPG Standard, as well as to the participants of the **Early Grade Reading Community of Practice**. We also thank the following organizations: UNICEF, iSPIRT, the Government of Sierra Leone, the Government of Norway, and the DPGA Secretariat.

*Image Credit: [Badge](https://thenounproject.com/search/?q=seal+of+approval&i=32270) by André Luiz from [the Noun Project](http://thenounproject.com/), released under a CC license.*

## :memo: License

This repository is primarily content, and it is licensed under a [Creative Commons Attribution ShareAlike 4.0 International License](LICENSE).

[![CC BY-SA 4.0][cc-by-sa-image]](LICENSE)

> This is a human-readable summary of (and not a substitute for) the license.
> 
> You are free to:
> * **Share** — copy and redistribute the material in any medium or format
> * **Adapt** — remix, transform, and build upon the material for any purpose, even commercially.
> 
> The licensor cannot revoke these freedoms as long as you follow the license terms.
> 
> * **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
> * **ShareAlike** — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.
>
> No additional restrictions — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.

[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
[code-of-conduct-shield]: https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg
