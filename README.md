# linux-how-to

1. **Ensure Your Repositories are Correct**:
   Make sure the `deb-src` lines in your `/etc/apt/sources.list` and any other files in `/etc/apt/sources.list.d/` are uncommented. This allows you to fetch source packages.

2. **Update Your Package Database**:
   ```bash
   sudo apt update
   ```

3. **Fetch the Source Package**:
   ```bash
   sudo apt source linux-hwe-5.15
   ```

After running this, you should have a directory in your current location with the Ubuntu-specific kernel source for your version. Navigate into this directory to compile or inspect the source.

It's worth noting that you might end up downloading a slightly newer revision if updates have been pushed to the repositories since you last updated. If you must have the *exact* version (5.15.0-83-generic), you might need to explore the Ubuntu package archives for that specific version.
