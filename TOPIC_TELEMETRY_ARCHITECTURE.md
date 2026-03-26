# TOPIC: Sovereign Telemetry Architecture (v1.2)
**Entity:** PointSav Digital Systems
**Protocol:** DS-ADR-06

## The Cyberphysical Stack (4-Tier Routing)
The telemetry system completely bypasses cloud-based data aggregation by utilizing a Multi-Tier Mirroring approach over encrypted tunnels.

1. **Ingest (Tier 2 Cloud):** Live Nginx relays capture organic JSON payloads at the edge and blindly route them to `10.50.0.2:8081` (PointSav) and `10.50.0.2:8082` (Woodfine).
2. **Transit (Cryptographic Tunnel):** Payloads traverse the `wg0` Wireguard mesh, penetrating the local firewall.
3. **Process (Tier 1 Execution Body):** The Rust `telemetry-daemon` (bound to `0.0.0.0`) ingests packets to local CSV ledgers on `laptop-a`. The `omni-matrix-engine` dynamically cross-references `GeoLite2-City.mmdb` to compile structural Markdown reports.
4. **Govern (Tier 1 Showcase):** The Control Node (iMac) executes the Master Diode (`pull_sovereign_telemetry.sh`) to physically extract the intelligence without ever touching the raw edge.
