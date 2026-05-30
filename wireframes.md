# Universal Carbon Intelligence Platform — Wireframes

## 1. Dashboard (Main Overview)

**Purpose:** High-level summary of carbon data, recent activity, alerts, and quick access to main modules.


---

**Dashboard — Abstract Screen Wireframe**

<div style="border:1px solid #b6d0e2; border-radius:18px; overflow:hidden; max-width:760px; margin:auto; font-family:'Inter',sans-serif; background:linear-gradient(135deg,#f9f9f9 80%,#e0f2fe 100%); box-shadow:0 8px 32px 0 rgba(34,60,80,0.12);">
    <div style="background:linear-gradient(90deg,#2563eb 60%,#38bdf8 100%); color:#fff; padding:20px 32px; display:flex; align-items:center; justify-content:space-between; box-shadow:0 2px 8px 0 rgba(34,60,80,0.10);">
        <span style="font-weight:700; font-size:1.3em; letter-spacing:0.5px; display:flex; align-items:center;"><span style="background:#fff2; border-radius:50%; padding:6px 12px; margin-right:12px; font-size:1.3em;">🌱</span>Logo</span>
        <nav style="display:flex; gap:28px; font-size:1.08em;">
            <span style="opacity:1; font-weight:600; border-bottom:2px solid #fff;">Dashboard</span><span style="opacity:0.85;">Ingest</span><span style="opacity:0.85;">Map</span><span style="opacity:0.85;">AI</span><span style="opacity:0.85;">Market</span><span style="opacity:0.85;">Profile</span>
        </nav>
        <span style="font-size:1.3em;">⚙️</span>
    </div>
    <div style="display:flex; gap:32px; padding:32px; background:linear-gradient(90deg,#e9f5ee 80%,#f0f9ff 100%);">
        <div style="flex:2;">
            <div style="display:flex; gap:20px; margin-bottom:32px;">
                <div style="background:#fff; border-radius:12px; flex:1; padding:20px 12px 18px 12px; text-align:center; box-shadow:0 2px 8px 0 rgba(34,60,80,0.07); border:1.5px solid #e0e7ef;">
                    <div style="font-size:2.2em; margin-bottom:2px;">🌍</div>
                    <div style="font-size:1.13em; font-weight:600; color:#2563eb;">Total CO₂</div>
                    <div style="font-size:1.35em; color:#059669; font-weight:700;">1,234,567 t</div>
                </div>
                <div style="background:#fff; border-radius:12px; flex:1; padding:20px 12px 18px 12px; text-align:center; box-shadow:0 2px 8px 0 rgba(34,60,80,0.07); border:1.5px solid #e0e7ef;">
                    <div style="font-size:2.2em; margin-bottom:2px;">📁</div>
                    <div style="font-size:1.13em; font-weight:600; color:#2563eb;">Projects</div>
                    <div style="font-size:1.35em; color:#059669; font-weight:700;">42</div>
                </div>
                <div style="background:#fff; border-radius:12px; flex:1; padding:20px 12px 18px 12px; text-align:center; box-shadow:0 2px 8px 0 rgba(34,60,80,0.07); border:1.5px solid #e0e7ef;">
                    <div style="font-size:2.2em; margin-bottom:2px;">⚠️</div>
                    <div style="font-size:1.13em; font-weight:600; color:#be123c;">Alerts</div>
                    <div style="font-size:1.35em; color:#be123c; font-weight:700;">3</div>
                </div>
                <div style="background:#fff; border-radius:12px; flex:1; padding:20px 12px 18px 12px; text-align:center; box-shadow:0 2px 8px 0 rgba(34,60,80,0.07); border:1.5px solid #e0e7ef;">
                    <div style="font-size:2.2em; margin-bottom:2px;">💹</div>
                    <div style="font-size:1.13em; font-weight:600; color:#2563eb;">Market Value</div>
                    <div style="font-size:1.35em; color:#2563eb; font-weight:700;">€1.2M</div>
                </div>
            </div>
            <div style="background:#fff; border-radius:12px; padding:24px 20px; margin-bottom:28px; min-height:80px; box-shadow:0 1px 4px 0 rgba(34,60,80,0.06); border:1.5px solid #e0e7ef;">
                <div style="font-weight:bold; margin-bottom:8px;">Recent Activity</div>
                <ul style="margin:0; padding-left:20px;">
                    <li>Project "Green Forest" updated</li>
                    <li>New dataset ingested</li>
                    <li>Alert: Data anomaly detected</li>
                </ul>
            </div>
            <div style="background:#fff; border-radius:12px; padding:24px 20px; min-height:60px; box-shadow:0 1px 4px 0 rgba(34,60,80,0.06); border:1.5px solid #e0e7ef;">
                <div style="font-weight:bold; margin-bottom:8px;">Quick Actions</div>
                <button style="margin-right:12px;">+ Add Data</button>
                <button>Export Report</button>
            </div>
        </div>
        <aside style="flex:1; display:flex; flex-direction:column; gap:20px;">
            <div style="background:#fff; border-radius:12px; padding:20px; box-shadow:0 1px 4px 0 rgba(34,60,80,0.06); border:1.5px solid #e0e7ef; display:flex; align-items:center; gap:16px;">
                <div style="width:48px; height:48px; border-radius:50%; background:linear-gradient(135deg,#bae6fd 60%,#f0f9ff 100%); display:flex; align-items:center; justify-content:center; font-size:2em;">👤</div>
                <div>
                  <div style="font-weight:600; color:#2563eb;">Jane Doe</div>
                  <div style="font-size:0.98em; color:#555;">Analyst</div>
                </div>
            </div>
            <div style="background:#fff; border-radius:12px; padding:20px; box-shadow:0 1px 4px 0 rgba(34,60,80,0.06); border:1.5px solid #e0e7ef;">
                <div style="font-weight:600; color:#2563eb; margin-bottom:6px;">Theme & Accessibility</div>
                <div><button style="margin-right:8px;">🌗</button> <button>Aa</button></div>
            </div>
        </aside>
    </div>
    <footer style="background:linear-gradient(90deg,#2563eb 60%,#38bdf8 100%); color:#fff; padding:14px 32px; text-align:center; font-size:1em; letter-spacing:0.2px; box-shadow:0 -2px 8px 0 rgba(34,60,80,0.08);">
        Theme Toggle | Accessibility | Legal
    </footer>
</div>

---

---

## 2. Data Ingestion / Upload

**Purpose:** Upload new datasets, monitor ingestion status, and view ETL logs.


---

**Data Ingestion / Upload — Abstract Screen Wireframe**

<div style="border:1px solid #ccc; border-radius:12px; overflow:hidden; max-width:700px; margin:auto; font-family:sans-serif; background:#f9f9f9;">
    <div style="background:#222; color:#fff; padding:16px 24px; display:flex; align-items:center; justify-content:space-between;">
        <span style="font-weight:bold; font-size:1.2em;">🌱 Logo</span>
        <nav style="display:flex; gap:24px;">
            <span>Dashboard</span><span>Ingest</span><span>Map</span><span>AI</span><span>Market</span><span>Profile</span>
        </nav>
        <span>⚙️</span>
    </div>
    <div style="padding:24px; background:#e9f5ee;">
        <div style="background:#fff; border-radius:8px; padding:24px; margin-bottom:24px; text-align:center;">
            <div style="font-size:2em;">⬆️</div>
            <div style="font-weight:bold; font-size:1.1em;">Upload Area</div>
            <div style="margin:8px 0;">Drag & Drop or <button>Select File</button></div>
            <div style="color:#555; font-size:0.95em;">Supported: CSV, GeoJSON, PDF, XLSX</div>
        </div>
        <div style="background:#fff; border-radius:8px; padding:20px; margin-bottom:24px;">
            <div style="font-weight:bold; margin-bottom:8px;">Ingestion Status</div>
            <table style="width:100%; border-collapse:collapse;">
                <tr style="background:#f0f0f0;"><th>Dataset</th><th>Status</th><th>Progress</th><th>Last Updated</th><th>Actions</th></tr>
                <tr><td>forest.csv</td><td>✅ Complete</td><td>100%</td><td>Today</td><td><button>View</button></td></tr>
                <tr><td>rivers.geojson</td><td>⏳ Processing</td><td>60%</td><td>1 min ago</td><td><button>Cancel</button></td></tr>
            </table>
        </div>
        <div style="background:#fff; border-radius:8px; padding:20px;">
            <div style="font-weight:bold; margin-bottom:8px;">ETL Logs / Error Console</div>
            <div style="font-family:monospace; background:#222; color:#fff; border-radius:6px; padding:12px; font-size:0.95em;">[INFO] Ingestion started...<br/>[ERROR] File format not supported: .txt</div>
        </div>
    </div>
    <footer style="background:#222; color:#fff; padding:12px 24px; text-align:center; font-size:0.95em;">
        Theme Toggle | Accessibility | Help
    </footer>
</div>

---

---

## 3. Geospatial Map / Analysis

**Purpose:** Visualize carbon projects, assets, and analytics on an interactive map.


---

**Geospatial Map / Analysis — Abstract Screen Wireframe**

<div style="border:1px solid #ccc; border-radius:12px; overflow:hidden; max-width:700px; margin:auto; font-family:sans-serif; background:#f9f9f9;">
    <div style="background:#222; color:#fff; padding:16px 24px; display:flex; align-items:center; justify-content:space-between;">
        <span style="font-weight:bold; font-size:1.2em;">🌱 Logo</span>
        <nav style="display:flex; gap:24px;">
            <span>Dashboard</span><span>Ingest</span><span>Map</span><span>AI</span><span>Market</span><span>Profile</span>
        </nav>
        <span>⚙️</span>
    </div>
    <div style="padding:24px; background:#e9f5ee;">
        <div style="background:#fff; border-radius:8px; padding:24px; margin-bottom:24px; display:flex; gap:24px; align-items:flex-start;">
            <div style="flex:3;">
                <div style="font-size:2em; text-align:center;">🗺️</div>
                <div style="font-weight:bold; font-size:1.1em; text-align:center;">Map View</div>
                <div style="margin:12px 0; text-align:center; color:#555;">World / Region Map</div>
            </div>
            <div style="flex:1;">
                <div style="font-size:1em; font-weight:bold; margin-bottom:8px;">Layer Controls</div>
                <div><input type="checkbox" checked> Projects<br><input type="checkbox"> Assets<br><input type="checkbox"> Analytics</div>
                <div style="margin-top:12px; font-size:1em; font-weight:bold;">Legend</div>
                <div style="color:#555;">🟢 Project<br>🔵 Asset<br>🟡 Alert</div>
                <div style="margin-top:12px; font-size:1em; font-weight:bold;">Search/Filter</div>
                <input type="text" placeholder="Search..." style="width:100%; padding:4px;">
            </div>
        </div>
        <div style="background:#fff; border-radius:8px; padding:20px;">
            <div style="font-weight:bold; margin-bottom:8px;">Project List / Details</div>
            <table style="width:100%; border-collapse:collapse;">
                <tr style="background:#f0f0f0;"><th>Name</th><th>Type</th><th>Status</th><th>Actions</th></tr>
                <tr><td>Green Forest</td><td>Project</td><td>Active</td><td><button>View</button></td></tr>
                <tr><td>Blue River</td><td>Asset</td><td>Inactive</td><td><button>View</button></td></tr>
            </table>
        </div>
    </div>
    <footer style="background:#222; color:#fff; padding:12px 24px; text-align:center; font-size:0.95em;">
        Theme Toggle | Accessibility | Map Data Source
    </footer>
</div>

---

---

## 4. Document Extraction / AI Insights

**Purpose:** Upload and extract data from documents, view AI-generated insights, and validate results.


---

**Document Extraction / AI Insights — Abstract Screen Wireframe**

<div style="border:1px solid #ccc; border-radius:12px; overflow:hidden; max-width:700px; margin:auto; font-family:sans-serif; background:#f9f9f9;">
    <div style="background:#222; color:#fff; padding:16px 24px; display:flex; align-items:center; justify-content:space-between;">
        <span style="font-weight:bold; font-size:1.2em;">🌱 Logo</span>
        <nav style="display:flex; gap:24px;">
            <span>Dashboard</span><span>Ingest</span><span>Map</span><span>AI</span><span>Market</span><span>Profile</span>
        </nav>
        <span>⚙️</span>
    </div>
    <div style="padding:24px; background:#e9f5ee;">
        <div style="background:#fff; border-radius:8px; padding:24px; margin-bottom:24px; text-align:center;">
            <div style="font-size:2em;">📄</div>
            <div style="font-weight:bold; font-size:1.1em;">Document Upload Area</div>
            <div style="margin:8px 0;"><button>Upload Document</button></div>
        </div>
        <div style="background:#fff; border-radius:8px; padding:20px; margin-bottom:24px;">
            <div style="font-weight:bold; margin-bottom:8px;">Extracted Data</div>
            <table style="width:100%; border-collapse:collapse;">
                <tr style="background:#f0f0f0;"><th>Field</th><th>Value</th><th>Confidence</th><th>Validate</th></tr>
                <tr><td>CO₂</td><td>1234 t</td><td>98%</td><td><input type="checkbox" checked></td></tr>
                <tr><td>Project</td><td>Green Forest</td><td>95%</td><td><input type="checkbox"></td></tr>
            </table>
        </div>
        <div style="background:#fff; border-radius:8px; padding:20px;">
            <div style="font-weight:bold; margin-bottom:8px;">AI Insights</div>
            <ul style="margin:0; padding-left:20px;">
                <li>Key Finding: High CO₂ reduction</li>
                <li>Warning: Data gap detected</li>
                <li>Suggestion: Upload more recent data</li>
            </ul>
        </div>
    </div>
    <footer style="background:#222; color:#fff; padding:12px 24px; text-align:center; font-size:0.95em;">
        Theme Toggle | Accessibility | Feedback
    </footer>
</div>

---

---

## 5. Market / Trading View

**Purpose:** Explore carbon market data, trade credits, and view price trends.


---

**Market / Trading View — Abstract Screen Wireframe**

<div style="border:1px solid #ccc; border-radius:12px; overflow:hidden; max-width:700px; margin:auto; font-family:sans-serif; background:#f9f9f9;">
    <div style="background:#222; color:#fff; padding:16px 24px; display:flex; align-items:center; justify-content:space-between;">
        <span style="font-weight:bold; font-size:1.2em;">🌱 Logo</span>
        <nav style="display:flex; gap:24px;">
            <span>Dashboard</span><span>Ingest</span><span>Map</span><span>AI</span><span>Market</span><span>Profile</span>
        </nav>
        <span>⚙️</span>
    </div>
    <div style="padding:24px; background:#e9f5ee;">
        <div style="display:flex; gap:24px; margin-bottom:24px;">
            <div style="background:#fff; border-radius:8px; flex:2; padding:16px; text-align:center;">
                <div style="font-size:2em;">💰</div>
                <div style="font-weight:bold; font-size:1.1em;">Market Overview</div>
                <div style="margin:8px 0; color:#555;">Price: €25.00 | Volume: 10k | Trend: 📈</div>
            </div>
            <div style="background:#fff; border-radius:8px; flex:1; padding:16px; text-align:center;">
                <div style="font-size:2em;">📊</div>
                <div style="font-weight:bold; font-size:1.1em;">Price Chart</div>
                <div style="margin:8px 0; color:#555;">Analytics & Trends</div>
            </div>
        </div>
        <div style="background:#fff; border-radius:8px; padding:20px;">
            <div style="font-weight:bold; margin-bottom:8px;">Trading Table</div>
            <table style="width:100%; border-collapse:collapse;">
                <tr style="background:#f0f0f0;"><th>Asset</th><th>Price</th><th>Change</th><th>Buy/Sell</th></tr>
                <tr><td>CO₂ Credit</td><td>€25.00</td><td>+2%</td><td><button>Buy</button> <button>Sell</button></td></tr>
                <tr><td>Forest Bond</td><td>€10.00</td><td>-1%</td><td><button>Buy</button> <button>Sell</button></td></tr>
            </table>
        </div>
    </div>
    <footer style="background:#222; color:#fff; padding:12px 24px; text-align:center; font-size:0.95em;">
        Theme Toggle | Accessibility | Market Info
    </footer>
</div>

---

---

## 6. User Profile / Settings

**Purpose:** Manage user info, preferences, API keys, and accessibility options.


---

**User Profile / Settings — Abstract Screen Wireframe**

<div style="border:1px solid #ccc; border-radius:12px; overflow:hidden; max-width:700px; margin:auto; font-family:sans-serif; background:#f9f9f9;">
    <div style="background:#222; color:#fff; padding:16px 24px; display:flex; align-items:center; justify-content:space-between;">
        <span style="font-weight:bold; font-size:1.2em;">🌱 Logo</span>
        <nav style="display:flex; gap:24px;">
            <span>Dashboard</span><span>Ingest</span><span>Map</span><span>AI</span><span>Market</span><span>Profile</span>
        </nav>
        <span>⚙️</span>
    </div>
    <div style="padding:24px; background:#e9f5ee;">
        <div style="background:#fff; border-radius:8px; padding:24px; margin-bottom:24px;">
            <div style="font-size:2em; text-align:center;">👤</div>
            <div style="font-weight:bold; font-size:1.1em; text-align:center;">User Info</div>
            <div style="margin:8px 0; text-align:center;">Name: Jane Doe<br>Email: jane@carbon.com<br>Role: Analyst<br>Org: GreenOrg</div>
        </div>
        <div style="display:flex; gap:24px; margin-bottom:24px;">
            <div style="background:#fff; border-radius:8px; flex:1; padding:16px;">
                <div style="font-weight:bold;">Preferences</div>
                <div>Theme: <button>🌗</button> | Language: <select><option>EN</option><option>NL</option></select></div>
                <div>Accessibility: <button>Aa</button></div>
            </div>
            <div style="background:#fff; border-radius:8px; flex:1; padding:16px;">
                <div style="font-weight:bold;">API Keys / Integrations</div>
                <div>API Key: <input type="text" value="••••••••" readonly></div>
                <div><button>Regenerate</button></div>
            </div>
        </div>
        <div style="background:#fff; border-radius:8px; padding:16px; text-align:center;">
            <button style="background:#c33; color:#fff; border:none; border-radius:6px; padding:8px 24px; font-weight:bold;">Logout</button>
        </div>
    </div>
    <footer style="background:#222; color:#fff; padding:12px 24px; text-align:center; font-size:0.95em;">
        Theme Toggle | Accessibility | Support
    </footer>
</div>

---

---

## 7. Theme Toggle & Accessibility

- Theme toggle always in header and footer
- High-contrast mode, font size controls, keyboard navigation
- All forms and tables: clear labels, focus indicators, ARIA attributes

---

## 8. Navigation & Layout (Mermaid Diagram)

```mermaid
flowchart TD
    A[Dashboard] --> B[Ingestion]
    A --> C[Map]
    A --> D[AI Extraction]
    A --> E[Market]
    A --> F[Profile]
    B -->|Upload| B1[Ingestion Status]
    C -->|Select Project| C1[Project Details]
    D -->|Upload Doc| D1[AI Insights]
    E -->|Trade| E1[Trading Table]
    F -->|Edit| F1[Preferences]
```

---

**Note:**
- All screens are responsive (mobile/tablet/desktop)
- Theme toggle and accessibility controls are always visible
- Use semantic HTML and ARIA for accessibility
- Wireframes are ready for UI design and frontend implementation
