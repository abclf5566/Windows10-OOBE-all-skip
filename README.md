# Windows10-OOBE-all-skip

# Sysprep Unattended Setup

This repository provides instructions for using `sysprep` with an unattended setup file `unattend.xml`. The default file path for `unattend.xml` is `%WINDIR%\System32\Sysprep\unattend.xml`.

## Prerequisites

1. Ensure you have administrative privileges on the machine.
2. Prepare the `unattend.xml` file with the necessary configurations.

## Instructions

1. Place the `unattend.xml` file in the following path:

```
%WINDIR%\System32\Sysprep\unattend.xml
```

2. Run the following `sysprep` command to initiate the setup with the unattended file:

- `/generalize`: Prepares the machine for imaging by removing system-specific data.
- `/oobe`: Initiates the Out-Of-Box Experience (OOBE) on the next boot.
- `/shutdown`: Shuts down the computer after sysprep completes.
- `/unattend`: Specifies the path to the unattended setup file.

```
sysprep /generalize /oobe /shutdown /unattend:%WINDIR%\System32\Sysprep\unattend.xml
```

## Account Configuration

In the `unattend.xml` file, you can configure account settings as follows:

- `<Name>Admin</Name>`: The name displayed when creating the account.
- `<DisplayName>Admin</DisplayName>`: The name displayed when logging in.

## Customizing for Different Languages

To change the system language settings, update the `SystemLocale`, `UserLocale`, and `UILanguage` elements in the `unattend.xml` file to match the desired language codes (e.g., en-US for English. default is ja-JP).

## Troubleshooting

- Ensure that the `unattend.xml` file is properly formatted and located in the correct directory.
- Check for any syntax errors in the XML configuration.

For more details on `sysprep` and `unattend.xml`, refer to the official Microsoft documentation.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
