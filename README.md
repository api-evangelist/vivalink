# VivaLNK (vivalink)

VivaLNK (Vivalink) is a connected-health company providing medical-grade wearable biosensors and a Biometrics Data Platform for remote patient monitoring (RPM), hospital-at-home, and decentralized clinical trials. Its wearable sensors capture ECG, heart rate, heart rate variability, respiratory rate, RR interval, body/axillary temperature, SpO2, blood pressure, and three-axis accelerometer data. Mobile edge clients read the sensors over Bluetooth Low Energy (BLE) and deliver data to the cloud over RESTful HTTPS services (Amazon API Gateway plus Amazon Kinesis for near-real-time ingestion). The platform exposes machine-to-machine (M2M) cloud web-service APIs, webhook push, HL7 FHIR integration, and bulk data-file downloads for EHR, CTMS, and clinical-application integration.

> **Partner-gated / modeled entry.** VivaLNK's developer surface is delivered through its SDK and Developer Program and is provided under license rather than published openly. There is no public base URL, OpenAPI document, or endpoint reference. The APIs, OpenAPI, and collections in this repository are **modeled** from VivaLNK's documented platform capabilities (M2M cloud web services, webhook support, FHIR support, bulk export) and are labeled as such; the base URL `https://api.vivalink.com` is a placeholder to confirm under the Developer Program.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/vivalink/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/vivalink/refs/heads/main/apis.yml)

## Tags

- Connected Health
- Remote Patient Monitoring
- RPM
- Wearables
- Biosensors
- Biometrics
- ECG
- Vital Signs
- Digital Health
- IoT
- Clinical Trials

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs

### VivaLNK Subjects API

Enroll and manage the subjects (patients / study participants) whose biometric data is captured by VivaLNK wearables - create, list, retrieve, update, and deactivate subjects, and associate them with a project, study, or care program. Endpoints are modeled from VivaLNK's documented M2M cloud web-service platform.

- **Human URL:** [https://www.vivalink.com/vitals-data-services](https://www.vivalink.com/vitals-data-services)
- **Base URL (modeled):** `https://api.vivalink.com`

#### Tags

- Subjects
- Patients
- Enrollment

#### Properties

- [Documentation](https://www.vivalink.com/vivalink-sdk)
- [Documentation](https://www.vivalink.com/vitals-data-services)
- [OpenAPI](openapi/vivalink-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vivalink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vivalink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### VivaLNK Devices API

Register and manage VivaLNK wearable biosensors - the Multi-Vital ECG patch, temperature patch, SpO2 sensor, and BP cuff - list devices, retrieve a device's status and firmware, and assign or unassign a device to a subject. Endpoints are modeled from VivaLNK's documented device-management capabilities.

- **Human URL:** [https://www.vivalink.com/wearable-products](https://www.vivalink.com/wearable-products)
- **Base URL (modeled):** `https://api.vivalink.com`

#### Tags

- Devices
- Sensors
- Wearables

#### Properties

- [Documentation](https://www.vivalink.com/vivalink-sdk)
- [Documentation](https://www.vivalink.com/wearable-products)
- [OpenAPI](openapi/vivalink-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vivalink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vivalink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### VivaLNK Vital Signs Data API

Retrieve continuous and summary biometric measurements collected from subjects' wearables - ECG waveform, heart rate, heart rate variability, RR interval, respiratory rate, body/axillary temperature, SpO2, blood pressure, and accelerometer/activity data - as time-ranged time series or aggregated summaries, plus bulk data-file exports for retrospective analysis. Near-real-time access is served over REST (backed by Amazon Kinesis) rather than a public streaming socket. Endpoints are modeled from VivaLNK's documented cloud data services.

- **Human URL:** [https://www.vivalink.com/vitals-data-services](https://www.vivalink.com/vitals-data-services)
- **Base URL (modeled):** `https://api.vivalink.com`

#### Tags

- Vital Signs
- ECG
- Heart Rate
- Temperature
- SpO2

#### Properties

- [Documentation](https://www.vivalink.com/vitals-data-services)
- [Documentation](https://aws.amazon.com/blogs/apn/next-gen-patient-monitoring-with-vivalinks-intelligent-biometrics-platform-and-aws/)
- [OpenAPI](openapi/vivalink-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vivalink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vivalink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### VivaLNK Webhooks API

Register webhook subscriptions so VivaLNK's platform pushes biometric data and alert events (for example threshold or arrhythmia notifications) to your HTTPS endpoint as they are produced - create, list, retrieve, update, and delete subscriptions. Webhook push is a documented VivaLNK Biometrics Data Platform capability; the endpoint shapes here are modeled.

- **Human URL:** [https://www.vivalink.com/vitals-data-services](https://www.vivalink.com/vitals-data-services)
- **Base URL (modeled):** `https://api.vivalink.com`

#### Tags

- Webhooks
- Subscriptions
- Events

#### Properties

- [Documentation](https://www.vivalink.com/vitals-data-services)
- [OpenAPI](openapi/vivalink-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vivalink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vivalink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### VivaLNK FHIR API

Access VivaLNK biometric data as HL7 FHIR resources (Patient, Device, Observation) for interoperability with EHR systems, CTMS, and clinical applications. FHIR support is a documented VivaLNK Biometrics Data Platform capability; the resource paths here are modeled on standard FHIR R4.

- **Human URL:** [https://www.vivalink.com/vitals-data-services](https://www.vivalink.com/vitals-data-services)
- **Base URL (modeled):** `https://api.vivalink.com/fhir`

#### Tags

- FHIR
- Interoperability
- EHR

#### Properties

- [Documentation](https://www.vivalink.com/vitals-data-services)
- [OpenAPI](openapi/vivalink-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vivalink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vivalink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## WebSocket Review

**Does VivaLNK expose a documented public WebSocket API?** No. VivaLNK's documented cloud surface is request/response REST over HTTPS (Amazon API Gateway) plus server-to-endpoint webhook push, with HL7 FHIR and bulk file export. Near-real-time delivery is handled internally by Amazon Kinesis Data Streams and read back over REST - there is no documented client-facing WebSocket (or SSE) stream. See [review.yml](review.yml).

## Common Properties

- [GitHub Organization](https://github.com/VivaLnk)
- [LinkedIn](https://www.linkedin.com/company/vivalnk-inc-)
- [Website](https://www.vivalink.com)
- [Documentation](https://www.vivalink.com/vivalink-sdk)
- [Sign Up / Contact](https://www.vivalink.com/contact)
- [Plans](plans/vivalink-plans-pricing.yml)
- [Rate Limits](rate-limits/vivalink-rate-limits.yml)
- [Fin Ops](finops/vivalink-finops.yml)
- [Blog](https://www.vivalink.com/blog)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
