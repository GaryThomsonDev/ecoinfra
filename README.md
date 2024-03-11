![Eco-Infra Logo](./logo.svg)

**ecoinfra** is a powerful tool that helps you predict, asses, and reduce the environmental impact of your cloud
infrastructure.
By integrating your existing or new IaC project you can harness predictive sustainability into your cloud operations.

Visit our website at [**Eco-Infra.com**](https://eco-infra.com) to learn more about how we're revolutionizing
eco-friendly cloud computing.

## 🚀 Getting Started

To start using the **ecoinfra** tool, follow these simple steps:

### Step 1: Download the Tool

1. Visit [**releases**](https://github.com/eco-infra/ecoinfra/releases) to download the **ecoinfra** tool for your
   supported operating system.
2. Once the download is complete, locate the downloaded file on your computer.

### Step 2: Set up Your API Key

1. Open your web browser and go to [**Eco-Infra.com**](https://eco-infra.com).
2. Log in to your Eco-Infra account or create one if you don't have an account already.
3. After logging in, navigate to your profile settings.
4. In your profile settings, look for the "API Key" section.
5. Click on "Create".
6. A unique API key will be generated for you. Copy this key to your clipboard.

### Step 3: Run the Tool
Run the tool in a supported CI environment

[GitHub Actions](https://github.com/marketplace/actions/eco-infra-action) 
```yaml
  - name: Eco-Infra
    uses: ecoinfra/ecoinfra-action@v1.1.2
    with:
    token: 'TOKEN'
    project-name: 'my-project'
    path: './terraform'
    apply: 'true'
```

Or Run the tool from your command line interface (CLI) or terminal.

```bash
$ ecoinfra-PLATFORM --token {{Token}} --project-name {{Unique Project Name}} {{Project Directory}}
```

An example:

```bash
$ ecoinfra-PLATFORM --token c3da55b6-b8a0-43ad-b513-a751e76553de --project-name "Production Account" ./prod
```
---
## 📖 Documentation

The tool requires two arguments and a path to your IaC project (Where you run terraform form):

- `--token` - Your unique API key.
- `--project-name` - A unique name for your project.
- `{{Project Directory}}` - The directory of your IaC project.

You will be required you to run terraform init before running the tool.

## Supported Providers

- AWS 🟢
- Azure 🔴
- GCP 🔴

## Supported IaC Tools

- Terraform 🟢
- OpenTofu 🔴
- Pulumi 🔴
- CloudFormation 🔴
---
# Running the tool from source
1. Clone the repository.
2. Install the dependencies.
3. Build the tool
4. Run the tool!

```bash
git clone git@github.com:eco-infra/ecoinfra.git 
npm i
npm run package
./build/ecoinfra-PLATFORM --token {{Token}} --project-name {{Unique Project Name}} {{Project Directory}}
```

# Contributing
Please read the contribution guidelines before contributing to the project. [CONTRIBUTING.md](./CONTRIBUTING.md)