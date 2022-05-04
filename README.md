## Release Information

- Solution Pack Version: 1.0.0
- Minimum Compatible FortiSOAR™ Version: 7.2.0
- Authored By: Fortinet
- Certified: No

## Overview

### Introduction

**Sunburst Attack Solution Pack** is designed to provide a set of investigation playbooks to hunt the indicators related to the Sunburst Attack.

Download IOC's from CSV file and Create Indicators in FortiSOAR™. Hunt the Sunburst Indicators using Fortinet's FortiEDR and Splunk.

Configure the Fortinet FortiEDR and Splunk connector and then trigger the **Sunburst IOC Hunt** playbook on **Hunt - Sunburst Attack** hunt record to Hunt Sunburst Indicators.

Refer to Simulation Scenario - "Sunburst Attack IOC Hunt" to experience the use case without any connector configuration.

### Usage

Refer to [Simulate Scenario documentation](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/docs/solution-pack-guide.md) to understand how to Simulate and Reset scenarios.

This Solution Pack ships with the following simulation scenarios.

#### 1. Scenario - Sunburst Attack IOC Hunt

The scenario generates a demo hunt record **Hunt - Sunburst Attack**.

Navigate to the generated hunt record and observe that the Hunt Time Range i.e Hunt Start Date and Hunt End Date to download the IOC from the specified URL.

**Sunburst IOC Hunt** : Launch **Sunburst IOC Hun** Playbook and observe various investigation activities such as

- Downloading IOCs from CSV file.
- Creating Indicators.
- Hunting Sunburst Indicators.
- Creating 'Sunburst' type Alert.

## Prerequisites

|**Solution Pack Name**|**Purpose**|**Doc Link**|
| :- | :- | :- |
|SOAR Framework 1.0.0|Require for Incident Response modules|[Click here](https://github.com/fortinet-fortisoar/solution-pack-soar-framework/blob/develop/README.md)|
|SOC Simulator 1.0.1|Require for Scenario Module and SOC Simulator connector| [Click here](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/README.md)|

## Contents

1. Connector(s)
    |**SN**|**Connector Name**|
    | :- | :- |
    |1|Fortinet FortiEDR|
    |2|Fortinet FortiGate|
    |3|Splunk|

     **Warning:** After deployment, this Solution Pack installs or upgrades the stated list of connectors.
2. Global Variable(s)
    - Demo_mode
    - QRadarTimeZone

3. Record Set(s)
    - Scenario: Sunburst Attack IOC Hunt
4. Playbook Collection(s)
    - 05 - Hunt - Sunburst (3):

    |**SN**|**Playbook Name**|**Description**|
    | :- | :- | :- |
    |1|Hunt Sunburst IOCs|Download IOCs from the threat intelligence feeds and hunt them|
    |2|Hunt Sunburst Indicator|Performs a hunt on the specified Sunburst indicators using Splunk and FortiEDR|
    |3|Block Sunburst Indicators|Blocks Sunburst indicators on Fortinet FortiGate and Fortinet FortiEDR|
    |4|Generate Demo Hunt Record|Generates Demo Hunt Record for Sunburst Attack IOC Hunt|

     **Warning:** It is recommended to clone these Playbooks before any customizations to avoid loss of information while upgrading the Solution Pack.
