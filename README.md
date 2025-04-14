# LogoTrust: A BIMI-based Logo Dataset

This repository contains a dataset of brand logos, domain names, and their mapping, generated by leveraging Brand Indicators for Message Identification (BIMI). The dataset is constructed using BIMI records, which associate brand logos with domain names through Mark Certificates.
This methodology provides a reliable and verifiable resource for various applications, including potentially phishing detection.

## Structure

The repository is organized as follows:

* `logos/`: This folder contains a set of directories each named after a brand name and contains a list of logo images corresponding to that brand name in SVG format. Each image is a unique, authenticated logo extracted from BIMI TXT records.
    
* `domain_names.json`: This file provides a mapping between brand names and their corresponding domain names (as they appear in mark certificates).


## Dataset Characteristics

The dataset includes:

* 1,680 brands
    
* 1,811 logos
    
* 2,821 domain names
    

## Methodology

The dataset was created by:

1.  Collecting domain names from various sources, including gTLD zone files, passive DNS data, Google certificate transparency logs, and the Tranco 5M list.
    
2.  Querying BIMI TXT records for each domain to obtain logo URLs and Mark Certificate URLs.
    
3.  Validating Mark Certificates to ensure the authenticity of the logo-domain name mapping.
4.  Deduplicating logos using SHA256 hashing to retain only unique logo images.

## Intended Use

This dataset can be used for:

* Developing and evaluating logo recognition solutions.
    
* Enhancing phishing detection systems by verifying the authenticity of brand logos.
    
* Research on brand identification and online trust.
    

## Limitations

* The dataset's coverage is limited by the current adoption rate of BIMI.
    
* Only logos published using the default BIMI selector are included.
    
* This dataset contains only one logo per domain name.

## Acknowledgements

This work is based on the paper "LogoTrust: Leveraging BIMI to Build a Validated Dataset of Brands, Domain Names, and Logos."