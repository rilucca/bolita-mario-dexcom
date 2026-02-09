# bolita-dexcom
Diabetes monitor and voice assistant for the Xiaozhi Bolita V2
# Bolita Dexcom Monitor 🩺
A custom package for the Xiaozhi "Bolita" to display real-time Dexcom glucose levels.

### 📝 Configuration Setup

To keep your credentials private, this project uses a `secrets.yaml` file. Update your **substitutions** section in `Ball-v2-3Mario.yaml` as follows:

```yaml
substitutions:
  # The system automatically builds your entities using your secrets.yaml
  user_name: !secret dexcom_username
  
  # Entity IDs are constructed automatically:
  glucose_value_entity: "sensor.${user_name}_glucose_value"
  glucose_trend_entity: "sensor.${user_name}_glucose_trend"

