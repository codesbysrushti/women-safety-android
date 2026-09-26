<div align="center">

<h1>🛡️ WomenSafety</h1>

<p>
<b>Personal Safety & Emergency SOS Application</b>
</p>

<p>
An Android application that uses shake detection to trigger an emergency SOS alert,
retrieve the device's available location, and send an SMS to a configured emergency contact.
</p>

<br>

<a href="https://github.com/codesbysrushti/women-safety-android">
<img src="https://img.shields.io/badge/View%20Project-GitHub-181717?style=for-the-badge&logo=github" alt="GitHub Repository">
</a>

<br><br>

<img src="https://img.shields.io/badge/Platform-Android-3DDC84?style=flat-square&logo=android&logoColor=white" alt="Android">
<img src="https://img.shields.io/badge/Language-Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java">
<img src="https://img.shields.io/badge/IDE-Android%20Studio-3DDC84?style=flat-square&logo=androidstudio&logoColor=white" alt="Android Studio">
<img src="https://img.shields.io/badge/Build-Gradle-02303A?style=flat-square&logo=gradle&logoColor=white" alt="Gradle">
<img src="https://img.shields.io/badge/Min%20SDK-24-blue?style=flat-square" alt="Minimum SDK">
<img src="https://img.shields.io/badge/Target%20SDK-36-blue?style=flat-square" alt="Target SDK">

</div>

<hr>

## 📌 Overview

WomenSafety is an Android application designed to provide a quick emergency-alert workflow when a user may not be able to interact with their phone normally.

The application monitors the device's accelerometer through a foreground service. When **five qualifying shakes** are detected within the configured timing window, the application triggers an SOS workflow.

The SOS workflow:

- Retrieves the device's available location.
- Creates a Google Maps location link when a location is available.
- Sends an emergency SMS to the configured contact.
- Displays an SOS notification.
- Plays an emergency siren.
- Activates phone vibration.

<hr>

## ✨ Features

<table>
<tr>
<th>Feature</th>
<th>Description</th>
</tr>

<tr>
<td><b>Shake-Based SOS</b></td>
<td>Detects five qualifying phone shakes to trigger the emergency workflow.</td>
</tr>

<tr>
<td><b>Location Retrieval</b></td>
<td>Uses GPS and network location providers to obtain the available device location.</td>
</tr>

<tr>
<td><b>Emergency SMS</b></td>
<td>Sends an automated emergency message to the configured contact.</td>
</tr>

<tr>
<td><b>Google Maps Location</b></td>
<td>Includes latitude and longitude in the emergency message together with a Maps link.</td>
</tr>

<tr>
<td><b>Foreground Service</b></td>
<td>Keeps shake detection active through an Android foreground service.</td>
</tr>

<tr>
<td><b>Emergency Notification</b></td>
<td>Displays a high-priority notification after an SOS is triggered.</td>
</tr>

<tr>
<td><b>SMS Status Tracking</b></td>
<td>Tracks SMS sent and delivery results through broadcast receivers.</td>
</tr>

<tr>
<td><b>Siren & Vibration</b></td>
<td>Provides local audio and vibration feedback when an SOS is triggered.</td>
</tr>

</table>

<hr>

## 🔄 How It Works

<table>
<tr>
<th>Step</th>
<th>Process</th>
</tr>

<tr>
<td><b>01</b></td>
<td>User enters an emergency contact number.</td>
</tr>

<tr>
<td><b>02</b></td>
<td>User enables location and grants the required permissions.</td>
</tr>

<tr>
<td><b>03</b></td>
<td>User starts the safety service.</td>
</tr>

<tr>
<td><b>04</b></td>
<td>The foreground service monitors the accelerometer.</td>
</tr>

<tr>
<td><b>05</b></td>
<td>Five qualifying shakes are detected within the configured time window.</td>
</tr>

<tr>
<td><b>06</b></td>
<td>The application obtains the latest available location.</td>
</tr>

<tr>
<td><b>07</b></td>
<td>An SOS SMS containing emergency information is sent to the configured contact.</td>
</tr>

<tr>
<td><b>08</b></td>
<td>The application displays an SOS notification, plays a siren, and vibrates the device.</td>
</tr>

</table>

<hr>

<h2>🔄 How It Works</h2>

<pre>
                    ┌─────────────────────┐
                    │   Open WomenSafety  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Enter Emergency     │
                    │ Contact Number      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Enable Location &   │
                    │ Required Permissions│
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   START SERVICE     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Accelerometer       │
                    │ Shake Detection     │
                    └──────────┬──────────┘
                               │
                         5 Shakes
                               │
                               ▼
                    ┌─────────────────────┐
                    │    SOS Triggered    │
                    └──────────┬──────────┘
                               │
                 ┌─────────────┴─────────────┐
                 ▼                           ▼
        ┌─────────────────┐         ┌─────────────────┐
        │ Retrieve        │         │ Emergency SMS   │
        │ Location        │────────▶│ Sent to Contact │
        └─────────────────┘         └─────────────────┘
                 │
                 ▼
        ┌──────────────────────┐
        │ SOS Notification     │
        │ Siren + Vibration    │
        └──────────────────────┘
</pre>

<hr>

<h2>🛠️ Technology Stack</h2>

<table>
<tr>
<th>Technology</th>
<th>Usage</th>
</tr>

<tr>
<td><strong>Java</strong></td>
<td>Application logic and Android components</td>
</tr>

<tr>
<td><strong>Android SDK</strong></td>
<td>Android platform APIs and device functionality</td>
</tr>

<tr>
<td><strong>Android Studio</strong></td>
<td>Application development environment</td>
</tr>

<tr>
<td><strong>XML</strong></td>
<td>User interface layouts and Android resources</td>
</tr>

<tr>
<td><strong>Accelerometer</strong></td>
<td>Shake detection</td>
</tr>

<tr>
<td><strong>LocationManager</strong></td>
<td>GPS and network location retrieval</td>
</tr>

<tr>
<td><strong>SmsManager</strong></td>
<td>Emergency SMS communication</td>
</tr>

<tr>
<td><strong>Foreground Service</strong></td>
<td>Continuous background safety monitoring</td>
</tr>

<tr>
<td><strong>Android Notifications</strong></td>
<td>Safety-service and SOS notifications</td>
</tr>

<tr>
<td><strong>Gradle</strong></td>
<td>Project build and dependency management</td>
</tr>

</table>

<hr>

<h2>📂 Project Structure</h2>

<pre>
WomenSafety/
│
├── app/
│   └── src/
│       ├── androidTest/
│       ├── main/
│       │   ├── java/
│       │   │   └── com/example/womensafety/
│       │   │       ├── MainActivity.java
│       │   │       ├── ShakeDetectorService.java
│       │   │       └── SMSHelper.java
│       │   │
│       │   ├── res/
│       │   │   ├── drawable/
│       │   │   ├── layout/
│       │   │   ├── mipmap/
│       │   │   ├── raw/
│       │   │   ├── values/
│       │   │   └── xml/
│       │   │
│       │   └── AndroidManifest.xml
│       │
│       └── test/
│
├── gradle/
│   └── libs.versions.toml
│
├── .gitignore
├── build.gradle.kts
├── gradle.properties
├── gradlew
├── gradlew.bat
├── README.md
└── settings.gradle.kts
</pre>

<hr>

<h2>📱 Application Components</h2>

<table>
<tr>
<th>Component</th>
<th>Responsibility</th>
</tr>

<tr>
<td><code>MainActivity.java</code></td>
<td>Handles the main interface, contact validation, permissions, location checks, and service start/stop controls.</td>
</tr>

<tr>
<td><code>ShakeDetectorService.java</code></td>
<td>Runs the foreground service, monitors the accelerometer, retrieves location, and triggers the SOS workflow.</td>
</tr>

<tr>
<td><code>SMSHelper.java</code></td>
<td>Handles emergency SMS transmission and sent/delivery status tracking.</td>
</tr>

<tr>
<td><code>activity_main.xml</code></td>
<td>Defines the application's main user interface.</td>
</tr>

<tr>
<td><code>AndroidManifest.xml</code></td>
<td>Declares application components, permissions, and the foreground service.</td>
</tr>

<tr>
<td><code>siren.mp3</code></td>
<td>Provides the emergency siren sound used after SOS activation.</td>
</tr>

</table>

<hr>

<h2>⚙️ Technical Configuration</h2>

<table>
<tr>
<th>Configuration</th>
<th>Value</th>
</tr>

<tr>
<td>Application ID</td>
<td><code>com.example.womensafety</code></td>
</tr>

<tr>
<td>Minimum SDK</td>
<td>Android API 24</td>
</tr>

<tr>
<td>Target SDK</td>
<td>Android API 36</td>
</tr>

<tr>
<td>Compile SDK</td>
<td>Android API 36.1</td>
</tr>

<tr>
<td>Java Compatibility</td>
<td>Java 11</td>
</tr>

<tr>
<td>Version Code</td>
<td>1</td>
</tr>

<tr>
<td>Version Name</td>
<td>1.0</td>
</tr>

<tr>
<td>Build System</td>
<td>Gradle</td>
</tr>

<tr>
<td>UI</td>
<td>Android XML</td>
</tr>

</table>

<hr>

<h2>🚀 Getting Started</h2>

<h3>Prerequisites</h3>

<p>Before running the project, make sure the following are installed:</p>

<ul>
<li>Android Studio</li>
<li>Android SDK</li>
<li>Compatible JDK</li>
<li>Android device or Android Emulator</li>
</ul>

<h3>Clone the Repository</h3>

<pre>
git clone https://github.com/codesbysrushti/women-safety-android.git
</pre>

<h3>Open the Project</h3>

<ol>
<li>Open Android Studio.</li>
<li>Select <strong>Open</strong>.</li>
<li>Select the <code>women-safety-android</code> project directory.</li>
<li>Allow Gradle synchronization to complete.</li>
<li>Connect an Android device or start an Android Emulator.</li>
<li>Click <strong>Run</strong>.</li>
</ol>

<hr>

<h2>🔐 Required Permissions</h2>

<table>
<tr>
<th>Permission</th>
<th>Purpose</th>
</tr>

<tr>
<td><code>SEND_SMS</code></td>
<td>Send emergency SMS messages</td>
</tr>

<tr>
<td><code>ACCESS_FINE_LOCATION</code></td>
<td>Access precise device location</td>
</tr>

<tr>
<td><code>ACCESS_COARSE_LOCATION</code></td>
<td>Access approximate device location</td>
</tr>

<tr>
<td><code>FOREGROUND_SERVICE</code></td>
<td>Run the safety monitoring service</td>
</tr>

<tr>
<td><code>VIBRATE</code></td>
<td>Provide emergency vibration feedback</td>
</tr>

<tr>
<td><code>POST_NOTIFICATIONS</code></td>
<td>Display notifications on supported Android versions</td>
</tr>

</table>

<p>
<strong>Note:</strong> The required permissions must be granted for the
corresponding features to operate.
</p>

<hr>

<h2>📍 Location Handling</h2>

<p>
The application checks whether location services are enabled before starting
the safety service.
</p>

<p>During operation, the application can use:</p>

<ul>
<li>GPS provider</li>
<li>Network location provider</li>
<li>Last known location</li>
<li>Location accuracy information</li>
</ul>

<p>When an SOS is triggered and a location is available, the SMS contains:</p>

<pre>
Emergency Alert
Location:
Google Maps link

Coordinates: latitude, longitude
Please call me &amp; come immediately!
</pre>

<p>
If a location cannot be obtained, the application sends an emergency message
asking the recipient to call the user immediately.
</p>

<hr>

<h2>📳 Shake Detection</h2>

<p>
The current implementation uses the Android accelerometer.
</p>

<table>
<tr>
<th>Setting</th>
<th>Current Value</th>
</tr>

<tr>
<td>Shake Threshold</td>
<td>800</td>
</tr>

<tr>
<td>Required Shakes</td>
<td>5</td>
</tr>

<tr>
<td>Minimum Shake Gap</td>
<td>500 ms</td>
</tr>

<tr>
<td>Shake Reset Window</td>
<td>4000 ms</td>
</tr>

</table>

<p>
The service ignores duplicate sensor readings that occur within the configured
minimum shake gap.
</p>

<p>
If the required number of shakes is reached before the reset window expires,
the SOS workflow is triggered.
</p>

<hr>

<h2>💬 Emergency SMS</h2>

<p>The emergency message can contain:</p>

<ul>
<li>SOS warning</li>
<li>Emergency alert information</li>
<li>Google Maps location link</li>
<li>Latitude and longitude</li>
<li>Request to call the user immediately</li>
</ul>

<p>
The application also registers callbacks to monitor whether the SMS was
successfully sent and delivered.
</p>

<hr>

<h2>⚠️ Important Notes</h2>

<p>
This application depends on Android device capabilities and system conditions.
</p>

<p>Functionality may be affected by:</p>

<ul>
<li>Location permissions</li>
<li>Location services</li>
<li>SMS permissions</li>
<li>Mobile network availability</li>
<li>SIM availability</li>
<li>Device sensor availability</li>
<li>Android background-service restrictions</li>
<li>Android version and manufacturer-specific restrictions</li>
<li>Device battery-management settings</li>
</ul>

<p>
<strong>Important:</strong> WomenSafety is an emergency-assistance project and
should not be considered a guaranteed replacement for official emergency
services.
</p>

<hr>

<h2>🔮 Future Improvements</h2>

<table>
<tr>
<th>Status</th>
<th>Improvement</th>
</tr>

<tr>
<td>☐</td>
<td>Multiple emergency contacts</td>
</tr>

<tr>
<td>☐</td>
<td>Configurable shake sensitivity</td>
</tr>

<tr>
<td>☐</td>
<td>Emergency-call integration</td>
</tr>

<tr>
<td>☐</td>
<td>Improved location handling</td>
</tr>

<tr>
<td>☐</td>
<td>Emergency notification history</td>
</tr>

<tr>
<td>☐</td>
<td>Improved accessibility</td>
</tr>

<tr>
<td>☐</td>
<td>Background-service optimization</td>
</tr>

<tr>
<td>☐</td>
<td>Additional Android-version testing</td>
</tr>

<tr>
<td>☐</td>
<td>Improved emergency-alert cancellation</td>
</tr>

<tr>
<td>☐</td>
<td>Additional safety features</td>
</tr>

</table>

<hr>

<h2>🧪 Testing</h2>

<p>
The project includes Android instrumented-test and unit-test source directories.
</p>

<p>Testing can be performed using:</p>

<ul>
<li>Android Emulator</li>
<li>Physical Android device</li>
<li>Different Android versions</li>
<li>Different device sensor configurations</li>
<li>Location enabled/disabled scenarios</li>
<li>SMS availability scenarios</li>
</ul>

<p>
For reliable testing of SMS and sensor behavior, a physical Android device
may be more appropriate than an emulator.
</p>

<hr>

<h2>🎯 Project Objective</h2>

<p>
The objective of <strong>WomenSafety</strong> is to demonstrate how Android
device capabilities can be combined to create a practical emergency-assistance
workflow.
</p>

<p>The project demonstrates:</p>

<ul>
<li>Android application development</li>
<li>Sensor integration</li>
<li>Accelerometer-based shake detection</li>
<li>Location services</li>
<li>SMS communication</li>
<li>Foreground services</li>
<li>Android runtime permissions</li>
<li>Notifications</li>
<li>Audio and vibration feedback</li>
<li>Gradle-based Android project management</li>
</ul>

<hr>

<h2>👩‍💻 Author</h2>

<div align="center">

<h3>Srushti Dubal</h3>

<p>
<strong>WomenSafety · Android Application · Personal Safety</strong>
</p>

<a href="https://github.com/codesbysrushti">
<img src="https://img.shields.io/badge/GitHub-codesbysrushti-181717?style=for-the-badge&logo=github" alt="GitHub">
</a>

</div>

<hr>

<div align="center">

<h3>⭐ Support the Project</h3>

<p>
If you find this project useful, consider giving the repository a star.
</p>

<a href="https://github.com/codesbysrushti/women-safety-android">
<img src="https://img.shields.io/github/stars/codesbysrushti/women-safety-android?style=for-the-badge&logo=github" alt="GitHub Stars">
</a>

<br><br>

<sub>Built with Android Studio &amp; Java</sub>

<br><br>

<sub>© Srushti Dubal</sub>

</div>
