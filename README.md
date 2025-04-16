# 📱 Parental App Time Limit

This is a simple parental control app designed to help manage and restrict app usage for children. It allows parents to define how much time a child can spend on certain apps and enables monitoring of app activity in a secure way.

##Screenshot
<img width="270" alt="Screenshot 2025-04-16 at 11 01 18 PM" src="https://github.com/user-attachments/assets/d5682bd4-8157-44a3-861e-4c6d7883b640" />




## 🧠 How It Works

The app supports two types of user modes:

- **Individual Mode** – For general users with no restrictions.
- **Child Mode** – Enables parental control features and app usage restrictions.

By default, the app is set to **Individual Mode** in the `AppDelegate`.

## 🔧 Changing Authorization Mode

To enable **Parental Control**, you need to change the authorization mode from `.individual` to `.child` and provide the appropriate child credentials.

### 👤 Default (Individual Mode)

```swift
AuthorizationCenter.shared.requestAuthorization(for: .individual)
```

### 👶 Switch to Child Mode (with Parental Control Enabled)

```swift
AuthorizationCenter.shared.requestAuthorization(for: .child)
```

Once in **Child Mode**, you can:

- Restrict access to certain apps.
- Set daily or weekly time limits.
- Track app usage.
- Lock apps during certain hours (e.g., bedtime or school time).

## 🛠 Setup Instructions

1. Clone or download the repository.
2. Open the project in Xcode.
3. Locate the `AppDelegate.swift` file.
4. Set the desired authorization mode (`.individual` or `.child`).
5. Run the app on a device or simulator.
6. If in **Child Mode**, make sure to authenticate with valid child credentials.

## 🔐 Security and Privacy

- All data and credentials are handled securely.
- Parent authentication is required to make changes in Child Mode.
- No third-party tracking or analytics are used.

## 🚧 Future Enhancements

- Add support for remote control by parents.
- Include notifications when time limits are exceeded.
- Provide reports and analytics of usage patterns.
- Support for multiple child profiles.

---

Feel free to contribute or raise an issue if you have suggestions or run into any problems!
