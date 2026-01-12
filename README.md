Sableye

Sableye automatically labels and scores cloud-native workloads and flows to enable policy-driven allow/deny decisions. The Labeler (Mistral 3) generates application labels from listening-service metadata; the Scorer (Gemma) evaluates flow metadata and returns a score with confidence to allow or deny traffic.
Features

    Labeler (Mistral 3): deterministic application labeling from listening-service metadata.
    Scorer (Gemma): confidence-based scoring of flows to allow/deny traffic.
    Locked-down backend: immutable cloud runtime with no SSH access and no application/payload logs.

Labeler — Mistral 3

Model: Mistral 3

Inputs

    Listening-service metadata: process name, package, service, port, protocol

Outputs

    Deterministic application label(s)
    Reason codes and confidence score

Scorer — Gemma

Model: Gemma (use subject to Gemma’s licensing and acceptable-use policies)

Inputs

    Flow metadata: source/destination labels, IP lists, ports, protocol, timestamps/context

Outputs

    Confidence score
    Reason

Security

    Frontend: HTTPS/TLS with CA certificates; strong cipher suites enforced.
    Backend: locked-down, immutable cloud instance — no SSH access, no key-based logins.
    No application/payload logs: backend does not persist raw application or payload logs.
    Network & data controls: strict firewall/network policies permit only required endpoints.
    Model compliance: use of Mistral 3 and Gemma follows their licensing and acceptable-use terms.

Model terms

    https://legal.mistral.ai/terms
    https://ai.google.dev/gemma/terms
