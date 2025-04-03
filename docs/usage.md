## Validate YAML Manifest

```bash
rai-compliance validate your_governance_manifest.yaml
```

## Loading a Governance Manifest

```py
from rai_compliance import GovernanceFramework

# Load from a YAML file containing laws, rules, and metrics
framework = GovernanceFramework.from_yaml("your_governance_manifest.yaml")

# Apply the framework to a model or API
compliance_report = framework.evaluate_compliance(model=my_model)
print(compliance_report.summary())
```

## Using Metrics Individually

```py
from rai_compliance.metrics import PIIChecksMetric

# Initialize the PII detection metric
pii_metric = PIIChecksMetric()

# Example text to evaluate
text = "Contact me at john.doe@example.com or call 123-456-7890."

# Evaluate the text for PII
detected_pii = pii_metric.evaluate(model=None, dataset=text)

# Print the detected PII entities
print("Detected PII entities:", detected_pii)
```
