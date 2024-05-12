# Vulnrichment

## What It Does
This tool fetches enriched CVE data directly from the CISA Vulnrichment GitHub repo. It can also generate a Markdown report for a given CVE.

## Setup
Build:
```bash
go build vulnrichment.go
```

## Usage
Run the tool with a CVE ID to fetch data:
```bash
./vulnrichment CVE-YYYY-NNNN
```
To generate a detailed report in Markdown format, use the `--report` flag:
```bash
./vulnrichment --report CVE-YYYY-NNNN
```

## Example
### Report
```bash
$ ./vulnrichment --report CVE-2015-2051
```
```markdown
# CVE Report
## CVE ID: The D-Link DIR-645 Wired/Wireless Router Rev. Ax with firmware 1.04b12 and earlier allows remote attackers to execute arbitrary commands via a GetDeviceSettings action to the HNAP interface.
### Date Published: 2015-02-13T00:00:00
### Description
- The D-Link DIR-645 Wired/Wireless Router Rev. Ax with firmware 1.04b12 and earlier allows remote attackers to execute arbitrary commands via a GetDeviceSettings action to the HNAP interface.
### References
- [http://securityadvisories.dlink.com/security/publication.aspx?name=SAP10051](http://securityadvisories.dlink.com/security/publication.aspx?name=SAP10051)
- [https://www.exploit-db.com/exploits/37171/](https://www.exploit-db.com/exploits/37171/)
- [http://www.securityfocus.com/bid/72623](http://www.securityfocus.com/bid/72623)
- [http://www.securityfocus.com/bid/74870](http://www.securityfocus.com/bid/74870)
### Exploitation Status
- Exploitation: N/A
```
### json
```bash
$ ./vulnrichment CVE-2015-2051
```
```json
{
  "containers": {
    "cna": {
      "affected": [
        {
          "product": "n/a",
          "vendor": "n/a",
          "versions": [
            {
              "status": "affected",
              "version": "n/a"
            }
          ]
        }
      ],
      "datePublic": "2015-02-13T00:00:00",
      "descriptions": [
        {
          "lang": "en",
          "value": "The D-Link DIR-645 Wired/Wireless Router Rev. Ax with firmware 1.04b12 and earlier allows remote attackers to execute arbitrary commands via a GetDeviceSettings action to the HNAP interface."
        }
      ],
      "problemTypes": [
        {
          "descriptions": [
            {
              "description": "n/a",
              "lang": "en",
              "type": "text"
            }
          ]
        }
      ],
      "providerMetadata": {
        "dateUpdated": "2016-12-29T18:57:01",
        "orgId": "8254265b-2729-46b6-b9e3-3dfca2d5bfca",
        "shortName": "mitre"
      },
      "references": [
        {
          "tags": [
            "x_refsource_CONFIRM"
          ],
          "url": "http://securityadvisories.dlink.com/security/publication.aspx?name=SAP10051"
        },
        {
          "name": "37171",
          "tags": [
            "exploit",
            "x_refsource_EXPLOIT-DB"
          ],
          "url": "https://www.exploit-db.com/exploits/37171/"
        },
        {
          "name": "72623",
          "tags": [
            "vdb-entry",
            "x_refsource_BID"
          ],
          "url": "http://www.securityfocus.com/bid/72623"
        },
        {
          "name": "74870",
          "tags": [
            "vdb-entry",
            "x_refsource_BID"
          ],
          "url": "http://www.securityfocus.com/bid/74870"
        }
      ],
      "x_legacyV4Record": {
        "CVE_data_meta": {
          "ASSIGNER": "cve@mitre.org",
          "ID": "CVE-2015-2051",
          "STATE": "PUBLIC"
        },
        "affects": {
          "vendor": {
            "vendor_data": [
              {
                "product": {
                  "product_data": [
                    {
                      "product_name": "n/a",
                      "version": {
                        "version_data": [
                          {
                            "version_value": "n/a"
                          }
                        ]
                      }
                    }
                  ]
                },
                "vendor_name": "n/a"
              }
            ]
          }
        },
        "data_format": "MITRE",
        "data_type": "CVE",
        "data_version": "4.0",
        "description": {
          "description_data": [
            {
              "lang": "eng",
              "value": "The D-Link DIR-645 Wired/Wireless Router Rev. Ax with firmware 1.04b12 and earlier allows remote attackers to execute arbitrary commands via a GetDeviceSettings action to the HNAP interface."
            }
          ]
        },
        "problemtype": {
          "problemtype_data": [
            {
              "description": [
                {
                  "lang": "eng",
                  "value": "n/a"
                }
              ]
            }
          ]
        },
        "references": {
          "reference_data": [
            {
              "name": "http://securityadvisories.dlink.com/security/publication.aspx?name=SAP10051",
              "refsource": "CONFIRM",
              "url": "http://securityadvisories.dlink.com/security/publication.aspx?name=SAP10051"
            },
            {
              "name": "37171",
              "refsource": "EXPLOIT-DB",
              "url": "https://www.exploit-db.com/exploits/37171/"
            },
            {
              "name": "72623",
              "refsource": "BID",
              "url": "http://www.securityfocus.com/bid/72623"
            },
            {
              "name": "74870",
              "refsource": "BID",
              "url": "http://www.securityfocus.com/bid/74870"
            }
          ]
        }
      }
    },
    "adp": [
      {
        "metrics": [
          {
            "cvssV3_1": {
              "scope": "UNCHANGED",
              "version": "3.1",
              "baseScore": 8.8,
              "attackVector": "ADJACENT",
              "baseSeverity": "HIGH",
              "vectorString": "CVSS:3.1/AV:A/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H",
              "integrityImpact": "HIGH",
              "userInteraction": "NONE",
              "attackComplexity": "LOW",
              "availabilityImpact": "HIGH",
              "privilegesRequired": "NONE",
              "confidentialityImpact": "HIGH"
            }
          },
          {
            "other": {
              "type": "ssvc",
              "content": {
                "id": "CVE-2015-2051",
                "role": "CISA Coordinator",
                "options": [
                  {
                    "Exploitation": "active"
                  },
                  {
                    "Automatable": "no"
                  },
                  {
                    "Technical Impact": "total"
                  }
                ],
                "version": "2.0.3",
                "timestamp": "2024-05-02T18:31:27.959147Z"
              }
            }
          },
          {
            "other": {
              "type": "kev",
              "content": {
                "dateAdded": "2022-02-10",
                "reference": "https://www.cisa.gov/known-exploited-vulnerabilities-catalog?search_api_fulltext=CVE-2015-2051"
              }
            }
          }
        ],
        "affected": [
          {
            "cpes": [
              "cpe:2.3:h:dlink:dir-645:*:*:*:*:*:*:*:*"
            ],
            "vendor": "dlink",
            "product": "dir-645",
            "versions": [
              {
                "status": "affected",
                "version": "*",
                "versionType": "custom",
                "lessThanOrEqual": "1.04b12"
              }
            ],
            "defaultStatus": "unknown"
          },
          {
            "cpes": [
              "cpe:2.3:o:dlink:dir-645_firmware:1.03:*:*:*:*:*:*:*"
            ],
            "vendor": "dlink",
            "product": "dir-645_firmware",
            "versions": [
              {
                "status": "affected",
                "version": "1.03",
                "versionType": "custom",
                "lessThanOrEqual": "1.04b12"
              }
            ],
            "defaultStatus": "unknown"
          }
        ],
        "problemTypes": [
          {
            "descriptions": [
              {
                "lang": "en",
                "type": "CWE",
                "cweId": "CWE-77",
                "description": "CWE-77 Improper Neutralization of Special Elements used in a Command ('Command Injection')"
              }
            ]
          }
        ],
        "providerMetadata": {
          "shortName": "CISAADP",
          "orgId": "8c464350-323a-4346-a867-fc54517fa145",
          "dateUpdated": "2024-05-02T18:40:39.885Z"
        }
      }
    ]
  },
  "cveMetadata": {
    "assignerOrgId": "8254265b-2729-46b6-b9e3-3dfca2d5bfca",
    "assignerShortName": "mitre",
    "cveId": "CVE-2015-2051",
    "datePublished": "2015-02-23T17:00:00",
    "dateReserved": "2015-02-23T00:00:00",
    "dateUpdated": "2016-12-29T18:57:01",
    "state": "PUBLISHED"
  },
  "dataType": "CVE_RECORD",
  "dataVersion": "5.0"
}
```
