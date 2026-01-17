# Power-Theft-Detection-System-PTDS
Power Theft Detection System-PTDS is an intelligent ML-based solution that detects electricity theft by analyzing real-time consumption patterns. It automates detection, replaces manual inspections, sends alerts, reduces revenue loss for utilities, ensures fair billing, and leverages scalable Google AI technologies for smart grid–ready deployment.



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Neural Nexus - Power Theft Detection System</title>
    <style>
        :root {
            --primary-bg: #0d1117;
            --card-bg: #161b22;
            --accent-blue: #58a6ff;
            --alert-red: #f85149;
            --text-main: #c9d1d9;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--primary-bg);
            color: var(--text-main);
            margin: 0;
            padding: 20px;
        }

        .header {
            border-bottom: 1px solid #30363d;
            padding-bottom: 10px;
            margin-bottom: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .dashboard-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .card {
            background-color: var(--card-bg);
            border: 1px solid #30363d;
            border-radius: 8px;
            padding: 20px;
        }

        .status-badge {
            background-color: var(--alert-red);
            color: white;
            padding: 5px 10px;
            border-radius: 4px;
            font-size: 0.8em;
            font-weight: bold;
        }

        .data-value {
            font-size: 2em;
            color: var(--accent-blue);
            margin: 10px 0;
        }

        .chart-placeholder {
            width: 100%;
            height: 150px;
            background: linear-gradient(90deg, #1f2937 25%, #111827 50%, #1f2937 75%);
            border-radius: 4px;
            margin-top: 15px;
            position: relative;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
        }

        th, td {
            text-align: left;
            padding: 12px;
            border-bottom: 1px solid #30363d;
        }

        .footer {
            margin-top: 40px;
            text-align: center;
            font-size: 0.9em;
            color: #8b949e;
        }
    </style>
</head>
<body>

    <div class="header">
        <h1>NEURAL NEXUS <span style="font-size: 0.5em; vertical-align: middle;">PTDS v1.0</span></h1>
        <div>Location: Sector 5, Mt Maple St.</div>
    </div>

    <div class="dashboard-grid">
        <div class="card">
            <h3>Live Consumption Dashboard</h3>
            <div class="data-value">8.2 kW</div>
            <p>Normal Range: 2-4 kW</p>
            <div class="chart-placeholder">
                <p style="padding: 60px; text-align: center;">[ Time-Series Data Visualization ]</p>
            </div>
            <p style="color: var(--alert-red);">Anomalies Detected: 3</p>
        </div>

        <div class="card">
            <div style="display: flex; justify-content: space-between;">
                <h3>Theft Alert Notification</h3>
                <span class="status-badge">SUSPECTED THEFT</span>
            </div>
            <p><strong>Meter ID:</strong> 10234</p>
            <p><strong>Anomaly:</strong> High Consumption Spike</p>
            <p><strong>Time:</strong> 03:15 PM</p>
            <hr style="border: 0.5px solid #30363d;">
            <p><strong>Recommendation:</strong> Investigate site and verify connection.</p>
            <button style="background: var(--accent-blue); border: none; padding: 10px; border-radius: 4px; cursor: pointer; width: 100%;">View Details</button>
        </div>
    </div>

    <div class="card" style="margin-top: 20px;">
        <h3>System Architecture Logs</h3>
        <table>
            <thead>
                <tr>
                    <th>Process</th>
                    <th>Technology</th>
                    <th>Status</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Data Acquisition</td>
                    <td>Smart Meter / Sensors</td>
                    <td style="color: #3fb950;">Active</td>
                </tr>
                <tr>
                    <td>Theft AI Algorithm</td>
                    <td>XGBoost / Vertex AI</td>
                    <td style="color: #3fb950;">Processing</td>
                </tr>
                <tr>
                    <td>Communication Module</td>
                    <td>GSM / IoT Cloud</td>
                    <td style="color: #3fb950;">Online</td>
                </tr>
            </tbody>
        </table>
    </div>

    <div class="footer">
        Powered by Google Vertex AI & TensorFlow Lite [cite: 97, 103]
    </div>

</body>
</html>
