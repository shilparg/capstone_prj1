# capstone_prj1
Here’s a refined, low-cost capstone tailored to your strengths, Shilpa—covering **IoT, Modbus, ML/AI, security, and DevOps** using AWS Free Tier and scalable design principles.

---

## 🌱 Capstone Title: “Secure Smart Factory Simulation with Modbus & Predictive Analytics on AWS”

### 🎯 Goal
Build a modular, audit-ready system that simulates industrial sensor behavior via Modbus, ingests data through IoT pipelines, predicts anomalies using ML/AI, and enforces DevOps and security best practices.

---

## 🧩 Architecture Overview

| Layer | Function | AWS Services |
|-------|----------|--------------|
| **Edge Simulation** | Modbus-based sensor emulation & fault injection | Python + `pymodbus`, ESP32/RPi |
| **IoT Ingestion** | Secure device communication & telemetry | AWS IoT Core, Greengrass, Device Defender |
| **Data Pipeline** | Stream + batch processing | AWS Lambda, Kinesis, Glue |
| **Storage** | Raw + processed data | Amazon S3 (Free Tier), DynamoDB |
| **ML/AI** | Predictive modeling & anomaly detection | SageMaker (spot), Lambda + scikit-learn |
| **Security** | IAM, encryption, audit | IAM roles, KMS, CloudTrail, Config |
| **DevOps** | CI/CD, IaC, monitoring | CodePipeline, Terraform, CloudWatch |

---

## 🔌 Modbus Use Cases

- **Sensor Emulation**: Simulate temperature, humidity, vibration via Modbus registers
- **Stress Testing**: Control thermal chamber and inject faults
- **Secure Gateway**: Route Modbus traffic through Greengrass with TLS
- **Audit Logging**: Capture Modbus transactions for compliance

---

## 🧠 ML/AI Use Cases

- **Anomaly Detection**: Identify outliers in sensor data
- **Predictive Maintenance**: Forecast equipment failure based on vibration/temperature trends
- **Explainability**: Use SHAP or feature importance to justify predictions

---

## 🔐 Security Highlights

- **IAM Least Privilege**: Scoped roles for Lambda, IoT, SageMaker
- **Encrypted Data**: S3 + DynamoDB with KMS
- **Audit Trails**: CloudTrail + Config for change tracking
- **Device Posture**: AWS IoT Device Defender for behavior anomalies

---

## ⚙️ DevOps Practices

- **Terraform IaC**: Deploy IoT Core, Lambda, IAM, S3
- **CI/CD Pipeline**: GitHub → CodePipeline → Lambda/SageMaker
- **Monitoring & Alerts**: CloudWatch metrics + SNS notifications

---

## 💰 Cost Optimization

- Use **Free Tier**: Lambda, S3, DynamoDB, CloudWatch
- **Spot Instances** for SageMaker training
- **Greengrass local ML inference** to reduce cloud calls
- **Athena** for serverless querying over S3

---

## 📁 Portfolio Deliverables

- ✅ Terraform scripts with comments
- ✅ Modbus simulation scripts + fault injection logs
- ✅ Architecture diagram with security annotations
- ✅ ML notebook with explainability metrics
- ✅ IAM policy snippets with governance rationale
- ✅ CI/CD pipeline YAML + screenshots
- ✅ README with use case mapping and cost breakdown

---

Would you like help drafting the README, refining the architecture diagram, or preparing Terraform modules for this? I can also help you annotate the Modbus flow for auditability and prepare QA critique scenarios for mentoring.

Fantastic, Shilpa. Let’s start with the core deliverables for your capstone portfolio. I’ll break it into modular pieces you can refine and showcase individually or as a cohesive project.

---

## 📘 README Draft: “Secure Smart Factory Simulation with Modbus & Predictive Analytics on AWS”

### 🔹 Overview
This project simulates a smart factory environment using Modbus-based sensor emulation, secure IoT ingestion, and predictive ML/AI analytics. It demonstrates scalable, low-cost architecture on AWS with full coverage of DevOps, security, and governance best practices.

### 🔹 Key Features

- **Modbus Simulation**: Python-based emulation of industrial sensors (temperature, vibration, humidity) with fault injection
- **IoT Pipeline**: Secure ingestion via AWS IoT Core and Greengrass
- **ML/AI Analytics**: Predictive modeling for anomaly detection and equipment failure
- **Security & Compliance**: IAM least privilege, encrypted data, audit trails
- **DevOps Integration**: Terraform IaC, CI/CD pipeline, CloudWatch monitoring

### 🔹 Architecture Diagram
> _[Insert annotated diagram here: Modbus → Greengrass → IoT Core → Lambda → S3/DynamoDB → SageMaker → QuickSight]_  
> _Include security zones, IAM boundaries, and fault injection paths._

### 🔹 Technologies Used

| Domain | Tools |
|--------|------|
| IoT & Modbus | Python, pymodbus, ESP32/RPi, AWS IoT Core |
| ML/AI | SageMaker, scikit-learn, SHAP |
| Security | IAM, KMS, CloudTrail, AWS Config |
| DevOps | Terraform, CodePipeline, CloudWatch, GitHub |

### 🔹 Cost Optimization

- Free Tier: Lambda, S3, DynamoDB, CloudWatch
- Spot Instances: SageMaker training
- Serverless: Athena for querying S3
- Greengrass: Local inference to reduce cloud calls

### 🔹 Folder Structure

```
├── terraform/
│   ├── iot_core.tf
│   ├── lambda.tf
│   ├── iam.tf
│   └── s3.tf
├── modbus_simulation/
│   ├── simulate_temp.py
│   ├── fault_injection.py
│   └── README.md
├── ml_model/
│   ├── train_model.ipynb
│   ├── explainability.ipynb
│   └── model.pkl
├── ci_cd/
│   ├── pipeline.yml
│   └── screenshots/
├── diagrams/
│   └── architecture.png
└── README.md
```

### 🔹 Governance Highlights

- IAM policies scoped per service with audit rationale
- CloudTrail logs reviewed for unauthorized access
- Device Defender alerts for abnormal Modbus behavior
- Terraform state stored securely with versioning

---

## ✅ Next Steps

Would you like me to:
- Refine the architecture diagram with security annotations?
- Prepare Terraform modules for IoT Core, Lambda, and IAM?
- Draft the Modbus simulation README with fault injection scenarios?
- Help with SHAP explainability integration in your ML notebook?

Let’s build this into a portfolio-ready showcase that reflects your leadership in integration/test, governance, and smart manufacturing.

Excellent, Shilpa. Let’s begin with the first three deliverables: **architecture diagram**, **Terraform modules**, and **Modbus simulation README**. These will form the backbone of your portfolio and showcase your integration/test leadership, governance maturity, and technical depth.

---

## 📊 1. Architecture Diagram: “Secure Smart Factory Simulation”

Here’s a modular layout you can refine in draw.io, Lucidchart, or PlantUML:

### 🔹 Diagram Layers

```
[Modbus Sensor Simulation]
    ↓
[Greengrass Connector]
    ↓
[AWS IoT Core] ←→ [Device Defender]
    ↓
[Lambda Stream Processor] ←→ [CloudWatch Logs]
    ↓
[S3 (raw)] ←→ [Athena]
[DynamoDB (processed)]
    ↓
[SageMaker (training/inference)]
    ↓
[QuickSight Dashboard]
    ↓
[SNS Alerts]
```

### 🔹 Security Annotations

- IAM roles scoped per service (color-coded)
- KMS encryption zones (S3, DynamoDB, SageMaker)
- CloudTrail + Config for audit boundaries
- Greengrass TLS tunnel for Modbus traffic

Would you like this diagram rendered in draw.io or PlantUML next?

---

## 🧱 2. Terraform Modules (Starter Snippets)

### 🔹 `iot_core.tf`

```hcl
resource "aws_iot_thing" "modbus_device" {
  name = "modbus_simulator"
}

resource "aws_iot_policy" "iot_policy" {
  name = "modbus_policy"
  policy = jsonencode({
    "Version": "2012-10-17",
    "Statement": [{
      "Effect": "Allow",
      "Action": ["iot:Connect", "iot:Publish", "iot:Receive", "iot:Subscribe"],
      "Resource": "*"
    }]
  })
}
```

### 🔹 `lambda.tf`

```hcl
resource "aws_lambda_function" "stream_processor" {
  function_name = "modbus_stream_handler"
  runtime       = "python3.9"
  handler       = "lambda_function.lambda_handler"
  role          = aws_iam_role.lambda_exec.arn
  filename      = "stream_handler.zip"
}
```

### 🔹 `iam.tf`

```hcl
resource "aws_iam_role" "lambda_exec" {
  name = "lambda_exec_role"
  assume_role_policy = jsonencode({
    "Version": "2012-10-17",
    "Statement": [{
      "Effect": "Allow",
      "Principal": { "Service": "lambda.amazonaws.com" },
      "Action": "sts:AssumeRole"
    }]
  })
}

resource "aws_iam_policy_attachment" "lambda_logs" {
  name       = "lambda_logs"
  roles      = [aws_iam_role.lambda_exec.name]
  policy_arn = "arn:aws:iam::aws:policy/service-role/AWSLambdaBasicExecutionRole"
}
```

Would you like me to expand this into a full module with outputs and variables next?

---

## 📘 3. Modbus Simulation README (Starter)

### 🔹 Purpose
Simulate industrial sensor behavior using Modbus TCP and inject faults to validate cloud ingestion, error recovery, and audit logging.

### 🔹 Setup

```bash
pip install pymodbus
```

### 🔹 Sample Script

```python
from pymodbus.client.sync import ModbusTcpClient

client = ModbusTcpClient('192.168.0.10')
client.write_register(100, 75)  # Simulate temperature = 75°C
response = client.read_holding_registers(100, 1)
print(f"Temperature: {response.registers[0]} °C")
client.close()
```

### 🔹 Fault Injection

```python
client.write_register(100, 999)  # Inject out-of-range value
```

### 🔹 Governance Notes

- All Modbus transactions logged to CloudWatch
- Faults trigger Lambda alerts and SNS notifications
- Device Defender monitors abnormal traffic patterns

---

Let me know which you'd like to refine next: the full Terraform module, the diagram rendering, or the ML notebook with SHAP explainability. We can also prep a QA critique scenario using fault injection logs.

Perfect, Shilpa. Let’s move forward with the next set of deliverables for your capstone portfolio:

---

## 🧭 1. Full Terraform Module Structure

Here’s a modular layout you can use across your repo:

### 🔹 `main.tf`

```hcl
module "iot_core" {
  source = "./modules/iot_core"
}

module "lambda_processor" {
  source = "./modules/lambda_processor"
}

module "iam_roles" {
  source = "./modules/iam_roles"
}
```

### 🔹 `modules/iot_core/main.tf`

```hcl
resource "aws_iot_thing" "modbus_device" {
  name = var.device_name
}

resource "aws_iot_policy" "iot_policy" {
  name = "modbus_policy"
  policy = file("${path.module}/iot_policy.json")
}
```

### 🔹 `modules/iot_core/variables.tf`

```hcl
variable "device_name" {
  type    = string
  default = "modbus_simulator"
}
```

### 🔹 `modules/lambda_processor/main.tf`

```hcl
resource "aws_lambda_function" "stream_processor" {
  function_name = var.function_name
  runtime       = "python3.9"
  handler       = "lambda_function.lambda_handler"
  role          = var.lambda_role_arn
  filename      = "${path.module}/stream_handler.zip"
}
```

Let me know if you’d like to add outputs, tagging, or S3/DynamoDB modules next.

---

## 🧠 2. ML Notebook with SHAP Explainability (Starter)

Here’s a minimal example using scikit-learn and SHAP:

```python
import pandas as pd
from sklearn.ensemble import RandomForestClassifier
import shap

# Load dataset
df = pd.read_csv("sensor_data.csv")
X = df.drop("anomaly", axis=1)
y = df["anomaly"]

# Train model
model = RandomForestClassifier()
model.fit(X, y)

# SHAP explainability
explainer = shap.TreeExplainer(model)
shap_values = explainer.shap_values(X)

# Visualize
shap.summary_plot(shap_values[1], X)
```

This shows which features (e.g., temperature, vibration) contribute most to anomaly predictions. You can annotate this for executive review and governance rationale.

---

## 📘 3. QA Critique Scenario: Fault Injection & Recovery

### 🔹 Scenario
Inject out-of-range Modbus value (`999°C`) and observe:

- Lambda logs capture anomaly
- SNS alert triggered
- Device Defender flags abnormal behavior
- SageMaker model predicts high anomaly score

### 🔹 Teaching Points

- Importance of boundary testing
- Audit trail validation via CloudTrail
- Recovery logic in Lambda (e.g., quarantine device, log incident)

---
Here’s a modular hardware setup for your capstone, Shilpa—designed to be **low-cost**, **realistic**, and aligned with your goals in IoT, Modbus simulation, ML/AI, and secure integration/test.

---

## 🧱 Core Hardware Components

| Purpose | Hardware | Notes |
|--------|----------|-------|
| **IoT Sensor Node** | ESP32 DevKit or Raspberry Pi 4 | ESP32 is cheaper (~SGD $10–15), supports Wi-Fi, Modbus via UART |
| **Modbus Simulation** | USB-to-RS485 adapter + PC or Pi | For Modbus RTU; use Python + `pymodbus` |
| **Environmental Sensors** | DHT22 (Temp/Humidity), MQ135 (Air Quality), Vibration sensor | Connect to ESP32 or Pi via GPIO |
| **Edge Gateway (optional)** | Raspberry Pi 4 or Pi Zero W | Acts as Greengrass host or Modbus TCP bridge |
| **Thermal Chamber (simulated)** | DIY setup with heat lamp + fan + relay | Controlled via GPIO or Modbus register |
| **Power Supply** | USB 5V adapter or battery pack | Ensure stable voltage for ESP32/Pi |
| **Connectivity** | Wi-Fi router or hotspot | Required for AWS IoT Core communication |

---

## 🧪 Optional Add-ons for QA & Stress Testing

- **Relay Module**: To simulate actuator control (e.g., fan, heater)
- **OLED Display**: For local sensor readouts
- **Breadboard + Jumper Wires**: For prototyping
- **Multimeter**: For debugging sensor connections

---

## 🧰 Local Development Setup

- **Laptop/PC**: For Python scripting, Terraform, ML notebooks
- **Python 3.9+**: With `pymodbus`, `boto3`, `scikit-learn`, `shap`
- **AWS CLI + Terraform**: For infrastructure deployment
- **VS Code**: With AWS Toolkit and GitHub integration

---

Would you like help wiring the sensors to ESP32, setting up Modbus RTU/TCP simulation, or preparing a Greengrass deployment guide? I can also help you annotate your hardware setup for portfolio presentation and audit readiness.

