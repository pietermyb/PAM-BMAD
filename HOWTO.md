# How to Build and Install Locally

This guide explains how to build the `PAM-bmad` project and install it on your local machine for use in other projects.

## Building the Project

To build the project, follow these steps:

1.  **Install Dependencies:**

    Open your terminal, navigate to the root directory of this project, and run:

    ```bash
    npm install
    ```

2.  **Run the Build Script:**

    After the dependencies are installed, run the build script:

    ```bash
    npm run build
    ```

    This will generate the necessary distributable files in the `dist` directory.

## Installing for Local Use

To use the `pam-bmad` command in other projects on your machine without publishing it to the npm registry, you can use `npm link`.

### Step 1: Create a Global Link

In the root directory of this project, run the following command to create a global symbolic link for the package:

```bash
npm link --force
```

**Note:** Using `--force` ensures that any existing links are overwritten with your latest changes.

This makes the `pam-bmad` command available system-wide, pointing to your local project directory.

**All in one command:**
```bash
npm install && npm run build && npm unlink pam-bmad && npm link --force
```

### Step 2: Use in a New Project

Once the link is created, you can use the package in any new project.

1.  Create a new directory for your project and navigate into it:

    ```bash
    mkdir /path/to/your-new-project
    cd /path/to/your-new-project
    ```

2.  Run the installer command:

    ```bash
    npx pam-bmad install
    ```

This will execute the installer from your local `pam-bmad` project and set up the necessary files and folders in your new project.

## Verification and Troubleshooting

### Verifying Your Installation

To ensure your local installation is working correctly with the latest changes:

1. **Test Local Installation:**
   ```bash
   # From the pam-bmad project root
   mkdir -p /tmp/test-install
   node tools/installer/bin/bmad.js install --full --directory /tmp/test-install
   ```

2. **Test Npx Installation:**
   ```bash
   # From any directory
   mkdir -p /tmp/test-npx
   npx pam-bmad install --full --directory /tmp/test-npx
   ```

3. **Verify Updated Content:**
   ```bash
   # Check that the installed user-guide.md contains your latest changes
   head -20 /tmp/test-install/.bmad-core/user-guide.md
   head -20 /tmp/test-npx/.bmad-core/user-guide.md
   ```

### Common Issues and Solutions

#### Issue: Old Version Being Installed

**Symptoms:** The installed files don't contain your latest changes.

**Solutions:**
1. **Clear npm cache:**
   ```bash
   npm cache clean --force
   ```

2. **Recreate the link:**
   ```bash
   npm unlink pam-bmad
   npm link --force
   ```

3. **Verify the link:**
   ```bash
   npm ls -g pam-bmad
   # Should show the path to your local project
   ```

#### Issue: Package Not Found

**Symptoms:** `npx pam-bmad install` fails with "package not found" error.

**Cause:** The package isn't published to npm yet, so npx can't find it.

**Solution:** Use the direct installation method:
```bash
# Clone or download the project
git clone <repository-url>
cd pam-bmad

# Install dependencies and build
npm install
npm run build

# Use direct installation
node tools/installer/bin/bmad.js install --full --directory /path/to/your-project
```

### Development Workflow

When making changes to the project:

1. **Make your changes** to the source files
2. **Rebuild if necessary:**
   ```bash
   npm run build
   ```
3. **Recreate the link:**
   ```bash
   npm link --force
   ```
4. **Test the installation:**
   ```bash
   # Test in a temporary directory
   mkdir -p /tmp/test-changes
   npx pam-bmad install --full --directory /tmp/test-changes
   ```
5. **Verify your changes** are included in the installation

### Publishing to npm

When ready to publish the package:

1. **Update version:**
   ```bash
   npm version patch  # or minor/major
   ```

2. **Publish:**
   ```bash
   npm publish
   ```

3. **Test published version:**
   ```bash
   # From a clean environment
   mkdir /tmp/test-published
   cd /tmp/test-published
   npx pam-bmad install --full
   ```

## Important Notes

- The `npm link` command creates a symbolic link, so changes to your source files are immediately available
- Always use `--force` with `npm link` to ensure you're using the latest version
- The installation process copies files from your local `bmad-core` directory, so make sure your changes are in the correct location
- If you're experiencing issues, try clearing the npm cache and recreating the link
