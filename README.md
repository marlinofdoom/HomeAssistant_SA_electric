[![](https://img.shields.io/github/release/marlinofdoom/HomeAssistant_SA_electric/all.svg?style=for-the-badge)](https://github.com/marlinofdoom/HomeAssistant_SA_electric/releases)
[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg?style=for-the-badge)](https://github.com/custom-components/hacs)
[![](https://img.shields.io/github/license/marlinofdoom/HomeAssistant_SA_electric?style=for-the-badge)](LICENSE)
[![](https://img.shields.io/badge/MAINTAINER-%40marlinofdoom-red?style=for-the-badge)](https://github.com/marlinofdoom)
[![](https://img.shields.io/badge/COMMUNITY-FORUM-success?style=for-the-badge)](https://community.home-assistant.io)

# HomeAssistant - Sensus Analytics Electricity Integration

A custom Home Assistant integration to monitor your electricity usage from Sensus Analytics, based on the water-only version by Zestysoft (https://github.com/zestysoft/sensus_analytics_integration/) and similar natural gas-only version by marlinofdoom (https://github.com/marlinofdoom/HomeAssistant_SA_gas)

## Features

- **Daily Usage**: Monitors daily electric usage.
- **Usage Unit**: Displays the unit of measurement for electric usage.
- **Meter Address**: Shows the address of the natural electric meter.
- **Last Read**: Timestamp of the last meter reading.
- **Meter Longitude**: Longitude coordinate of the meter's location.
- **Meter ID**: Unique identifier for the natural electric meter.
- **Meter Latitude**: Latitude coordinate of the meter's location.
- **Meter Odometer**: The total cumulative usage recorded by the meter.
- **Billing Usage**: Total usage amount that has been billed.
- **Billing Cost**: Total cost of the billed usage.
- **Daily Fee**: Daily fee based on usage.
- **Last Hour Usage**: Electric usage for the last hour from the previous day.
- **Last Hour Temperature**: Temperature data (in °F) for the last hour from the previous day.
- **Last Hour Timestamp**: Timestamp of the last hour's data from the previous day.

## Installation via HACS

### **Prerequisites**

- **HACS (Home Assistant Community Store)**: Make sure HACS is installed in your Home Assistant instance. If not, follow the [HACS Installation Guide](https://hacs.xyz/docs/installation/prerequisites).

### **Steps to Install**

1. **Open Home Assistant UI**

   Navigate to your Home Assistant instance in your web browser.

2. **Access HACS**

   - Click on "**HACS**" in the sidebar.

3. **Add Custom Repository**

   - In HACS, go to the "**Integrations**" tab.
   - Click on the "**⋮**" (three dots) menu in the top right corner and select "**Custom repositories**".

4. **Add the Sensus Analytics Repository**

   - **Repository URL**: `https://github.com/marlinofdoom/HomeAssistant_SA_electric`
   - **Category**: Select "**Integration**" from the dropdown menu.
   - Click "**Add**".

5. **Install the Integration**

   - After adding the repository, return to the "**Integrations**" tab in HACS.
   - Search for "**Sensus Analytics Integration**".
   - Click on the integration and then click "**Install**".
   - Wait for HACS to download and install the integration. You should see a confirmation message once it's complete.

6. **Restart Home Assistant**

   - After installation, it's essential to restart Home Assistant to load the new integration.
   - Go to "**Configuration**" > "**Settings**" > "**System**" > "**Restart**".
   - Confirm the restart.

7. **Configure the Integration via Home Assistant UI**

   - Once Home Assistant has restarted, navigate to "**Configuration**" > "**Integrations**".
   - Click the "**+ Add Integration**" button in the bottom right corner.
   - Search for "**Sensus Analytics**" and select "**Sensus Analytics Integration**".
   - Follow the prompts to enter your credentials and settings:
     - **Base URL**: Enter the base URL for your Sensus Analytics API (e.g., `https://<your_city>.sensus-analytics.com/`).
     - **Username**: Your Sensus Analytics account username.
     - **Password**: Your Sensus Analytics account password.
     - **Account Number**: Your Sensus Analytics account number.
     - **Electric Meter Number**: Your electric meter number.
     - **Electric Unit Type**: Choose which unit type you want the data to be used by Home Assistant.
     - **Electric Commodity Price**: Price per kWh for electricity purchased from utility.
     - **Electric Solar Credit Price**: (Optional) Price per kWh for electricity sold to utility (i.e. from a solar installation).
     - **Electric Service Fee**: Price the electric company charges just to have service.

   - Click "**Submit**" to finalize the configuration.

## Sensor Entities

Below are the sensor entities created by this integration:

- `sensor.sensus_analytics_electric_daily_usage`: Daily electric usage.
- `sensor.sensus_analytics_electric_usage_unit`: Native unit of measurement chosen by Sensus Analytics.
- `sensor.sensus_analytics_electric_meter_address`: Street address of the electric meter.
- `sensor.sensus_analytics_electric_last_read`: Timestamp of the last meter reading.
- `sensor.sensus_analytics_electric_meter_longitude`: Longitude coordinate of the meter's location.
- `sensor.sensus_analytics_electric_meter_id`: Unique identifier for the electric meter.
- `sensor.sensus_analytics_electric_meter_latitude`: Latitude coordinate of the meter's location.
- `sensor.sensus_analytics_electric_meter_odometer`: Total cumulative usage recorded by the meter.
- `sensor.sensus_analytics_electric_billing_usage`: Total usage amount that has been billed.
- `sensor.sensus_analytics_electric_billing_cost`: Total cost of the billed usage.
- `sensor.sensus_analytics_electric_daily_fee`: Daily fee based on usage.
- `sensor.sensus_analytics_electric_last_hour_usage`: Electric usage for the last hour from the previous day.
- `sensor.sensus_analytics_last_hour_temperature`: Temperature for the last hour from the previous day.
- `sensor.sensus_analytics_last_hour_timestamp`: Timestamp of the last hour's data from the previous day.

## License

[Apache 2.0](LICENSE)