# Visualization of TR-03105 Certificates

## Description

Map of generated certificates and their interrelationship - required for conformity testing of eMRTDS with EACv1 according to specifications of TR-03105 <https://www.bsi.bund.de/EN/Publications/TechnicalGuidelines/TR03105/BSITR03105.html>. Map is generated using graphviz <http://www.graphviz.org/>. Recommended layout `neato` or `(s)fdp`.

Connections between objects are defined by the following link types:

- **golden**: correctly issued signatur/child object; arrow points to child object
- **blue**: incorrectly issued signature/child object; `T` points to child object
- **red**: defines private-public key pair; `o` points to both objects
- `CVCA_CERT_00` and `CVCA_KEY_00`: representation of root object during personalization

## Usage

```bash
neato -Tpng tr03105p32v13_cert-map.dot -o tr03105p32v13_cert-map.png
```

## Changelog

### v0.2 - 2014-02-19

#### changed

- corrected typos
- corrected link in `cert.set.11`

### v0.1 - 2014-02-14

#### added

- default layout definitions
- adding certificate sets/links for Terminal Authentication from [TR-03105 Part 3.2 v1.3](<https://www.bsi.bund.de/EN/Publications/TechnicalGuidelines/TR03105/BSITR03105.html>)
