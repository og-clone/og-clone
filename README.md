# Exodus Wallet Clone - C# WPF Application

This is a visual replica of the Exodus cryptocurrency wallet interface built using C# and WPF (Windows Presentation Foundation).

## Features

- **Exact Visual Replica**: Matches the Exodus wallet design with dark theme, colors, and layout
- **Interactive UI**: Click between different cryptocurrencies (Bitcoin, Ethereum, Litecoin, Dogecoin, Solana, Cardano)
- **Dynamic Display**: Shows balance, USD values, and cryptocurrency-specific colors
- **Action Buttons**: Send, Receive, and Exchange buttons (placeholder functionality)
- **Responsive Design**: Proper window controls and draggable interface

## Requirements

- **Visual Studio 2022** or later
- **.NET 8.0 SDK** (or later)
- **Windows 10/11** (WPF is Windows-only)

## How to Build and Run

### Option 1: Using Visual Studio
1. Open Visual Studio 2022
2. Click "Open a project or solution"
3. Navigate to the `ExodusWallet` folder and open `ExodusWallet.csproj`
4. Press **F5** or click "Start Debugging" to build and run

### Option 2: Using Command Line
1. Open Command Prompt or PowerShell
2. Navigate to the `ExodusWallet` folder:
   ```bash
   cd ExodusWallet
   ```
3. Build the project:
   ```bash
   dotnet build
   ```
4. Run the application:
   ```bash
   dotnet run
   ```

### Option 3: Create Executable
1. Navigate to the project folder
2. Publish the application:
   ```bash
   dotnet publish -c Release -r win-x64 --self-contained true
   ```
3. The executable will be in: `bin\Release\net8.0-windows\win-x64\publish\ExodusWallet.exe`

## Project Structure

```
ExodusWallet/
├── MainWindow.xaml          # Main UI layout and styling
├── MainWindow.xaml.cs       # Code-behind with functionality
├── App.xaml                 # Application resources and startup
├── App.xaml.cs             # Application code-behind
├── ExodusWallet.csproj     # Project configuration
└── README.md               # This file
```

## How to Use

1. **Launch the application** - You'll see the main Exodus-style interface
2. **View Portfolio** - The total portfolio value is displayed at the top
3. **Select Cryptocurrencies** - Click on any cryptocurrency in the left sidebar:
   - Bitcoin (default selection)
   - Ethereum
   - Litecoin
   - Dogecoin
   - Solana
   - Cardano
4. **View Details** - The main area shows the selected crypto's balance and USD value
5. **Action Buttons** - Click Send, Receive, or Exchange (shows placeholder messages)
6. **Window Controls** - Use the minimize, maximize, and close buttons in the top-right

## Technical Details

- **Framework**: WPF (.NET 8.0)
- **Language**: C# 12.0
- **UI Pattern**: MVVM-like with code-behind
- **Styling**: XAML with custom styles and resources
- **Colors**: Exact color matching with Exodus wallet
- **Icons**: Unicode cryptocurrency symbols

## Customization

### Adding New Cryptocurrencies
1. Open `MainWindow.xaml.cs`
2. Add new entry to the `InitializeCryptoData()` method
3. Add corresponding UI element in `MainWindow.xaml` in the CryptoList section

### Changing Colors/Theme
1. Modify colors in `MainWindow.xaml` resources section
2. Update `App.xaml` global resources
3. Adjust individual cryptocurrency colors in the code-behind

### Adding Real Functionality
To add actual cryptocurrency functionality, you would need to:
- Integrate with cryptocurrency APIs
- Add wallet management logic
- Implement secure key storage
- Add transaction processing

## Security Notice

⚠️ **This is a visual clone only** - No real cryptocurrency functionality is implemented. This application:
- Does NOT handle real cryptocurrencies
- Does NOT store private keys
- Does NOT connect to blockchain networks
- Is for educational/demonstration purposes only

## License

This project is for educational purposes. Exodus is a trademark of Exodus Movement Inc.

## Screenshots

The application replicates the exact Exodus wallet interface including:
- Dark theme with proper color schemes
- Bitcoin-focused main display
- Sidebar with cryptocurrency list
- Action buttons and pending transaction alerts
- Professional window styling

---

**Note**: This application requires Windows and cannot be run on macOS or Linux due to WPF framework limitations.
