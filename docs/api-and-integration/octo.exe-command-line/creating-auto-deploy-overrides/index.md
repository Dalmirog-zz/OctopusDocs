---
title: Creating auto deploy overrides
description: Using the Octo.exe command line tool to create automatic deployment release overrides.
position: 12
---

[Octo.exe](/docs/api-and-integration/octo.exe-command-line/index.md) can be used to create automatic deployment release overrides.

```bash
octo create-autodeployoverride [<options>]
```

Where `[<options>]` is any of:

**create-autodeployoverride options**

```text
Auto deploy release override: 
      --project=VALUE        Name of the project
      --environment=VALUE    Name of an environment the override will apply 
                             to. Specify this argument multiple times to add 
                             multiple environments.
      --version, --releaseNumber=VALUE
                             Release number to use for auto deployments.
      --tenant=VALUE         [Optional] Name of a tenant the override will 
                             apply to. Specify this argument multiple times 
                             to add multiple tenants or use `*` wildcard for 
                             all tenants.
      --tenanttag=VALUE      [Optional] A tenant tag used to match tenants 
                             that the override will apply to. Specify this 
                             argument multiple times to add multiple tenant 
                             tags
Common options: 
      --server=VALUE         The base URL for your Octopus server - e.g., 
                             http://your-octopus/
      --apiKey=VALUE         Your API key. Get this from the user profile 
                             page.
      --user=VALUE           [Optional] Username to use when authenticating 
                             with the server.
      --pass=VALUE           [Optional] Password to use when authenticating 
                             with the server.
      --configFile=VALUE     [Optional] Text file of default values, with one 
                             'key = value' per line.
      --debug                [Optional] Enable debug logging
      --ignoreSslErrors      [Optional] Set this flag if your Octopus server 
                             uses HTTPS but the certificate is not trusted on 
                             this machine. Any certificate errors will be 
                             ignored. WARNING: this option may create a 
                             security vulnerability.
      --enableServiceMessages
                             [Optional] Enable TeamCity or Team Foundation 
                             Build service messages when logging.
```

## Basic example {#Creatingautodeployoverrides-Basicexample}

The following will create an automatic deployment release override for version 1.3.0 of the project *HelloWorld* to the environment *Development*:

```bash
Octo create-autodeployoverride --project HelloWorld --environment Development --version 1.3.0 --server http://octopus/ --apikey API-ABCDEF123456
```

## Tenanted example (by name) {#Creatingautodeployoverrides-Tenantedexample(byname)}

The following will create an automatic deployment release override for version 1.3.0 of the project *HelloWorld* to the environment *Development* for the tenant *Acme*:

```bash
Octo create-autodeployoverride --project HelloWorld --environment Development --tenant Acme --version 1.3.0 --server http://octopus/ --apikey API-ABCDEF123456
```

## Tenanted example (by tags) {#Creatingautodeployoverrides-Tenantedexample(bytags)}

The following will create an automatic deployment release override for version 1.3.0 of the project *HelloWorld* to the environment *Development* for all tenants with the *Hosting/Cloud* tag:

```bash
Octo create-autodeployoverride --project HelloWorld --environment Development --tenanttag Hosting/Cloud --version 1.3.0 --server http://octopus/ --apikey API-ABCDEF123456
```
