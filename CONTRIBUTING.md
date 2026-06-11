# 🤝 Contributing to Telegram Auto Gift Buyer

Thank you for your interest in contributing to Telegram Auto Gift Buyer! This document provides guidelines and instructions for contributing.

---

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Getting Started](#getting-started)
- [Development Setup](#development-setup)
- [Coding Guidelines](#coding-guidelines)
- [Submitting Changes](#submitting-changes)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Features](#suggesting-features)
- [Community](#community)

---

## Code of Conduct

### Our Pledge

We are committed to providing a welcoming and inspiring community for all. Please be respectful and considerate in your interactions.

### Our Standards

**Positive behavior includes:**
- ✅ Using welcoming and inclusive language
- ✅ Being respectful of differing viewpoints
- ✅ Gracefully accepting constructive criticism
- ✅ Focusing on what is best for the community
- ✅ Showing empathy towards others

**Unacceptable behavior includes:**
- ❌ Harassment or discriminatory language
- ❌ Trolling or insulting comments
- ❌ Public or private harassment
- ❌ Publishing others' private information
- ❌ Other unethical or unprofessional conduct

---

## How Can I Contribute?

### 💻 Code Contributions

- Fix bugs
- Implement new features
- Improve performance
- Refactor code
- Write tests

### 📝 Documentation

- Improve README and guides
- Write tutorials
- Create examples
- Translate documentation
- Fix typos and errors

### 🐛 Bug Reports

- Report issues
- Provide reproduction steps
- Test bug fixes

### 💡 Feature Requests

- Suggest new features
- Discuss improvements
- Share use cases

### 🎨 Design

- Create UI mockups
- Design icons and graphics
- Improve user experience

### 🌍 Translations

- Translate interface
- Localize documentation
- Review translations

---

## Getting Started

### Prerequisites

Before contributing, ensure you have:

- **Git** installed
- **GitHub account** created
- **Development environment** set up (see below)
- **Basic knowledge** of:
  - C# / .NET
  - WPF / XAML
  - Telegram API
  - Git workflow

### First-Time Contributors

New to open source? Check out:
- [How to Contribute to Open Source](https://opensource.guide/how-to-contribute/)
- [First Timers Only](https://www.firsttimersonly.com/)

Look for issues labeled:
- `good-first-issue` - Perfect for newcomers
- `help-wanted` - We need assistance
- `beginner-friendly` - Easy to tackle

---

## Development Setup

### 1. Fork the Repository

Click the "Fork" button on GitHub to create your copy.

### 2. Clone Your Fork

```bash
git clone https://github.com/YOUR-USERNAME/telegram-auto-gift-buyer.git
cd telegram-auto-gift-buyer
```

### 3. Add Upstream Remote

```bash
git remote add upstream https://github.com/original/telegram-auto-gift-buyer.git
```

### 4. Install Dependencies

**Required Software:**
- Visual Studio 2022 (Community or higher)
- .NET 8.0 SDK
- Git for Windows
- NuGet Package Manager

**Install NuGet Packages:**
```bash
dotnet restore
```

### 5. Create Development Branch

```bash
git checkout -b feature/your-feature-name
```

**Branch naming conventions:**
- `feature/` - New features
- `bugfix/` - Bug fixes
- `hotfix/` - Critical fixes
- `docs/` - Documentation updates
- `refactor/` - Code refactoring
- `test/` - Test additions

---

## Coding Guidelines

### Code Style

We follow standard C# conventions:

**General Rules:**
- Use PascalCase for class names and methods
- Use camelCase for local variables
- Use UPPER_CASE for constants
- Use meaningful names
- Keep methods under 50 lines
- One class per file

**Example:**
```csharp
public class GiftManager
{
    private const int MAX_RETRY_ATTEMPTS = 3;
    private readonly TelegramClient _client;

    public async Task<bool> SendGiftAsync(string recipientId, GiftType giftType)
    {
        // Implementation
    }
}
```

### Comments

- Write self-documenting code
- Add comments for complex logic
- Use XML documentation for public APIs

```csharp
/// <summary>
/// Sends a gift to the specified recipient
/// </summary>
/// <param name="recipientId">Telegram user ID</param>
/// <param name="giftType">Type of gift to send</param>
/// <returns>True if successful, false otherwise</returns>
public async Task<bool> SendGiftAsync(string recipientId, GiftType giftType)
{
    // Complex logic explanation
}
```

### Error Handling

Always use proper error handling:

```csharp
try
{
    await SendGiftAsync(recipient, gift);
}
catch (TelegramApiException ex)
{
    _logger.LogError(ex, "Failed to send gift to {Recipient}", recipient);
    throw;
}
catch (Exception ex)
{
    _logger.LogCritical(ex, "Unexpected error in gift sending");
    throw new GiftSendingException("Gift sending failed", ex);
}
```

### Testing

Write tests for new features:

```csharp
[TestMethod]
public async Task SendGift_ValidRecipient_ReturnsSuccess()
{
    // Arrange
    var giftManager = new GiftManager(mockClient.Object);
    
    // Act
    var result = await giftManager.SendGiftAsync("12345", GiftType.Premium);
    
    // Assert
    Assert.IsTrue(result);
}
```

---

## Submitting Changes

### 1. Commit Your Changes

Write clear, concise commit messages:

```bash
git add .
git commit -m "Add gift transfer fee calculator

- Implement 25-star transfer cost calculation
- Add UI for transfer fee display
- Include tests for fee calculation
- Update documentation

Fixes #123"
```

**Commit message format:**
```
Short summary (50 chars or less)

Detailed description if needed:
- What changed
- Why it changed
- Any breaking changes

References: #issue-number
```

### 2. Push to Your Fork

```bash
git push origin feature/your-feature-name
```

### 3. Create Pull Request

1. Go to GitHub repository
2. Click "New Pull Request"
3. Select your branch
4. Fill out PR template:
   - **Title:** Clear, descriptive
   - **Description:** What, why, how
   - **Screenshots:** If UI changes
   - **Testing:** How you tested
   - **Related Issues:** Link issues

**PR Template Example:**

```markdown
## Description
Brief description of changes

## Motivation
Why this change is needed

## Changes Made
- Added X feature
- Fixed Y bug
- Improved Z performance

## Testing
- [ ] Unit tests pass
- [ ] Manual testing completed
- [ ] No regressions found

## Screenshots
(if applicable)

## Related Issues
Fixes #123
Relates to #456
```

### 4. Code Review Process

- Maintainers will review your PR
- Address feedback and comments
- Make requested changes
- Push updates to same branch
- PR will be merged when approved

---

## Reporting Bugs

### Before Reporting

1. **Search existing issues** - May already be reported
2. **Try latest version** - Bug might be fixed
3. **Reproduce the bug** - Ensure it's consistent
4. **Gather information** - Logs, screenshots, etc.

### Bug Report Template

```markdown
**Description**
Clear description of the bug

**Steps to Reproduce**
1. Go to '...'
2. Click on '...'
3. Scroll down to '...'
4. See error

**Expected Behavior**
What should happen

**Actual Behavior**
What actually happens

**Screenshots**
If applicable

**Environment**
- OS: Windows 10 Pro 21H2
- App Version: 2.0.0
- .NET Version: 8.0
- Telegram Account Type: Premium

**Additional Context**
Any other relevant information

**Logs**
```
Paste relevant logs here
```

**Possible Fix**
(if you have ideas)
```

---

## Suggesting Features

### Before Suggesting

1. **Check existing requests** - May already exist
2. **Consider scope** - Fits project goals?
3. **Think about users** - Benefit to community?

### Feature Request Template

```markdown
**Feature Description**
Clear description of proposed feature

**Problem It Solves**
What problem does this address?

**Proposed Solution**
How should it work?

**Alternatives Considered**
Other approaches you've thought about

**Use Cases**
Real-world scenarios where this helps

**Implementation Notes**
Technical considerations (if applicable)

**Mockups/Examples**
Visual examples if relevant
```

---

## Development Workflow

### Keeping Your Fork Updated

```bash
# Fetch latest from upstream
git fetch upstream

# Merge into your main branch
git checkout main
git merge upstream/main

# Update your feature branch
git checkout feature/your-feature
git rebase main
```

### Running Tests

```bash
# Run all tests
dotnet test

# Run specific test
dotnet test --filter FullyQualifiedName~SendGiftAsync

# Run with coverage
dotnet test /p:CollectCoverage=true
```

### Building

```bash
# Debug build
dotnet build

# Release build
dotnet build -c Release

# Publish
dotnet publish -c Release -r win-x64 --self-contained
```

### Debugging

- Use Visual Studio debugger
- Set breakpoints
- Inspect variables
- Check logs in `%APPDATA%\TelegramAutoGiftBuyer\logs\`

---

## Community

### Communication Channels

- **GitHub Discussions** - General discussions
- **GitHub Issues** - Bug reports, feature requests
- **Discord** - Real-time chat
- **Telegram Group** - Community support

### Getting Help

- Read documentation first
- Search existing issues
- Ask in Discord/Telegram
- Tag maintainers if urgent

### Maintainers

Current maintainers:
- @maintainer1 - Lead developer
- @maintainer2 - UI/UX
- @maintainer3 - Documentation

### Response Times

- **Bug reports:** 24-48 hours
- **Feature requests:** 1 week
- **Pull requests:** 3-7 days
- **Security issues:** 24 hours

---

## Recognition

Contributors will be:
- ✨ Listed in CONTRIBUTORS.md
- 🏆 Credited in release notes
- 🎖️ Given contributor badge
- 💬 Mentioned on social media

Top contributors may become maintainers!

---

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

## Questions?

Have questions about contributing?

- 📧 Email: contribute@example.com
- 💬 Discord: [Join Server](https://discord.gg/example)
- 📖 Docs: [Contributing Guide](https://github.com/yourusername/telegram-auto-gift-buyer/wiki/Contributing)

---

**Thank you for contributing to Telegram Auto Gift Buyer!** 🎉

Every contribution, no matter how small, makes a difference!

[← Back to README](./README.md)
