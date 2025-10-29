# westover.services

Service discovery and gateway for self-hosted services running on westover.xyz and westover.dev.

## Purpose

This site provides a central hub for accessing various self-hosted services that don't fit into other categories:
- System monitoring (Netdata)
- Development tools (Penpot, web-based SSH)
- API services (Ghost Hunter, Skin Vault)
- Experimental projects

## Architecture

- **Public repo**: This repo (`neherdata/westover.services`) - public-facing landing page
- **Private repo**: `neherdata/westover_services` - backend configuration and service orchestration
- **Access control**: Most services protected by Cloudflare Access with GitHub OAuth

## Infrastructure

Services run on:
- **westover.xyz** (100.86.176.6) - Primary app server, AMD Ryzen 7 PRO, 28GB RAM
- **westover.dev** (coming soon) - Additional capacity for future services

## Services

### Active
- [Netdata](https://netdata.westover.xyz) - System monitoring
- [Penpot](https://design.westover.dev) - Design tool
- [Ghost Hunter API](https://westover.xyz) - AI detection API
- [Skin Vault API](https://linked.skin) - NSFW detection API

### Coming Soon
- Web-based SSH terminal
- Additional experimental services

## Access

Most services require:
1. GitHub account
2. Member of `neherdata` organization OR explicit access grant
3. Cloudflare Access authentication

## Development

To add a new service:
1. Configure in private `westover_services` repo
2. Update this landing page with service card
3. Set up Cloudflare Access policy
4. Deploy via Ansible/GitHub Actions
