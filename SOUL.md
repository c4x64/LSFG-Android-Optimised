# SOUL.md - Core Development Principles

## Mission
Develop LSFG-X (LSFG-Android-Optimised) as the premier frame generation solution for Android with:
- Root/Shizuku integration for enhanced performance
- 4x stability mode for all devices
- Esports mode with ultra-low latency
- Comprehensive mid-range GPU support (Mali, Exynos, Dimensity)
- Upstream compatibility maintenance

## Development Workflow

### Before Pushing to Git:
1. **Accumulate Meaningful Changes** - Never push after a single small change
2. **Bundle Related Features** - Group related functionality together
3. **Test Thoroughly** - Ensure all backends compile and basic functionality works
4. **Update Documentation** - Keep Ai.md and README files current
5. **Verify Build** - Confirm CMake configuration is correct

### Feature Development Cycle:
1. Implement core functionality
2. Add platform-specific optimizations
3. Create test cases or verification steps
4. Update all documentation
5. Review code quality (naming, modularity, comments)
6. THEN push to git

### Current Status:
- ✅ HAL interface implemented
- ✅ Platform detection for Mali/Exynos/Dimensity/Adreno
- ✅ Optimization profiles created
- ✅ 4x stability mode framework
- ✅ Conditional compilation for Root/Shizuku
- ⏳ Esports mode (TODO)
- ⏳ Actual Vulkan hooking logic (TODO)
- ⏳ Shizuku IPC implementation (TODO)
- ⏳ NPU acceleration (TODO)

### Next Features to Implement (Before Next Push):
1. **Esports Mode** - Ultra-low latency pipeline with minimal buffering
2. **Vulkan Hook Implementation** - Actual root-level frame capture
3. **Shizuku IPC Layer** - Real IPC communication with Shizuku service
4. **Frame Pacing Algorithm** - Advanced timing for smooth 4x operation
5. **GPU-Specific Shader Optimizations** - Custom shaders for each GPU vendor
6. **Real-time Performance HUD** - Monitoring overlay for frame times
7. **Shader Cache System** - Reduce stutter on mid-range devices
8. **Memory Management** - Aggressive caching for low-end devices

### Code Quality Standards:
- snake_case for C++ files/functions
- camelCase for Java/Kotlin
- Modular design (no monolithic functions)
- Preprocessor guards for all platform-specific code
- Comprehensive comments for complex logic
- PR-ready documentation for each module

### Git Hygiene:
- Meaningful commit messages
- Logical grouping of changes
- Update Ai.md with each session
- Only push when substantial progress is made

---
*This file defines the soul of the project - our commitment to quality, performance, and user experience.*
