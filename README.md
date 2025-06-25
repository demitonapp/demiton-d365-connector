# Demiton Governance Connector for Dynamics 365

[![License: MIT](https://img.shields.io/badge/License-MIT-teal.svg)](https://opensource.org/licenses/MIT)
[![Status: In Development](https://img.shields.io/badge/status-in%20development-orange.svg)](https://github.com/demitonapp/demiton-d365-connector)
[![Compatibility: D365 SCM](https://img.shields.io/badge/Dynamics%20365-Supply%20Chain-blue.svg)](https://dynamics.microsoft.com/en-us/supply-chain-management/)

This repository contains the open-source components for integrating the **Demiton Industrial Operations Platform** directly into **Microsoft Dynamics 365 Supply Chain Management**.

The goal of this connector is to bridge the critical gap between your enterprise ERP system and the operational technology (OT) running on your factory floor.

---

## The Problem: The Disconnected Asset

Your Dynamics 365 Asset Management module is a powerful tool for tracking the financial and maintenance lifecycle of your equipment. It can tell you an asset's purchase date, its maintenance schedule, and its depreciation value.

But it can't answer the most critical questions for a regulated manufacturer:

-   What is the **exact version of the PLC code** that was running on this asset during Production Order #75B?
-   Can you provide an **unbreakable audit trail** of every parameter change made to this asset last week?
-   How can you prove to a **TGA or GMP auditor** that this asset is in its validated "Golden Record" state?

This information lives in a separate, disconnected world. This connector brings that world directly into Dynamics 365.

## The Solution: An Embedded Governance Hub

This solution provides a set of components that embed Demiton's active governance capabilities directly into the D365 UI. The V1 release focuses on adding a new **"Operational Governance"** tab to the main **Asset** form.

From this new tab, a user can instantly see:
-   A complete list of all associated **Function Blocks** (the version-controlled code and configurations).
-   The designated **"Golden Record"** for the asset.
-   A full history of all **Deployment Requests** and **Deployment Logs**.
-   A direct link to the asset's detailed **Audit Trail** in the Demiton platform.

![Screenshot of the D365 Asset form with the new "Operational Governance" tab showing Demiton data]

## Technical Architecture

This connector is built using the standard Microsoft Power Platform toolchain. It consists of:

1.  **A Model-Driven Power App:** Provides the UI for the embedded "Operational Governance" tab.
2.  **Power Automate Flows:** Act as the secure middleware, making authenticated API calls to the Demiton backend to fetch and display data.
3.  **A D365 Solution File (`.zip`):** A package containing all the necessary components (the app, flows, and form customizations) for easy, one-click installation into a customer's D365 environment.

## Getting Started

Using this connector requires an active account on the [Demiton SaaS Platform](https://demiton.io).

The complete, packaged solution file will be available for download from the [Releases page](https://github.com/demitonapp/demiton-d365-connector/releases) and eventually from **Microsoft AppSource**.

Our official [documentation](https://demiton.io/docs/d365-connector) provides a full step-by-step guide for installation and configuration.

## Contributing

This is an open-source project. While the core Demiton platform is proprietary, we believe in transparency for the components that integrate with our partners' systems. We welcome community contributions, bug reports, and feature requests. Please see our `CONTRIBUTING.md` file for guidelines.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.