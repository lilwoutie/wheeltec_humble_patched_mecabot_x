
### Key Notes:
1. **Why this `.gitignore`?**
   - Excludes ROS-specific build artifacts (`build/`, `install/`, `log/`)
   - Ignores auto-generated `src/CMakeLists.txt` (created by `colcon`)
   - Includes standard ignores for Python cache, binaries, and editors

2. **ROS 2 Special Considerations:**
   - Use `--symlink-install` in build: Allows editing Python files without rebuilding
   - `rosdep install`: Handles system dependencies automatically
   - Source `setup.bash`: Required for every new terminal session

3. **Before Committing:**
   ```bash
   # Run from project root:
   git add .
   git commit -m "Initial ROS 2 Humble project setup"
   git push origin main
