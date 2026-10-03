# Vulnerable Testing Environments

Docker lab environments for validating old CVEs.

| CVE | Plugin | Affected | Template PR |
|---|---|---|---|
| CVE-2024-8425 | WooCommerce Ultimate Gift Card | <= 2.6.0 | [#13100](https://github.com/projectdiscovery/nuclei-templates/pull/13100) |
| CVE-2016-15042 | Frontend File Manager, N-Media Post Front-end Form | < 4.0, < 1.1 | [#13077](https://github.com/projectdiscovery/nuclei-templates/pull/13077) |

## Warning

These environments are intentionally vulnerable. Run them only on a local machine or an isolated network, never on a host reachable from the internet.

## Layout

```
CVE-2024-8425/    # WordPress + vulnerable Ultimate Gift Card
CVE-2016-15042/   # WordPress + both vulnerable plugins
```

## Usage

```sh
cd CVE-2024-8425
docker compose up -d
```

Tear down with `docker compose down -v`.

## License

Licensed under MIT. Third-party plugins keep their own licenses.
