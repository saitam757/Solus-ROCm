# Solus - ROCm Packaging
Trying to create packaging scripts for the [AMD Compute Stack](https://github.com/RadeonOpenCompute/ROCm) for Solus Linux eopkg,

Using [Gentoo](https://github.com/justxi/rocm) and [Arch](https://aur.archlinux.org/packages/?K=farnoy&SeB=m) packaging tries as templates for resolving dependency issues.

| Package  | Information | Status |
| ------------- | ------------- |------------- |
| [Roct](https://github.com/saitam757/Solus-ROCm/tree/master/roct)  | [ROCT-Thunk-Interface](https://github.com/RadeonOpenCompute/ROCT-Thunk-Interface/tree/roc-2.7.0)  | :heavy_check_mark: |
| [numactl](https://github.com/saitam757/Solus-ROCm/tree/master/numactl)  | Dependency of ROCT-Thunk-Interface  | :heavy_check_mark: |
| [Rocr](https://github.com/saitam757/Solus-ROCm/tree/master/rocr)  | [ROCR-Runtime](https://github.com/RadeonOpenCompute/ROCR-Runtime) | :heavy_check_mark: |



4) Rocminfo:    ROCm Application for Reporting System Info 
                Status of building: Package created.
                
            "lseopkg rocminfo-1.0.0-1-1-x86_64.eopkg" yields: 
                /usr/bin/rocm_agent_enumerator
                /usr/bin/rocminfo
                
5) rocm_bandwidth_test: Bandwidth test for ROCm 
                        Status of building: Package created.
                        
            "lseopkg rocm_bandwidth_test-2.5.0-1-1-x86_64.eopkg" yields:
                 /usr/bin/rocm_bandwidth_test
                 
6) z3: Z3 is a theorem prover. Dependency for LLVM, Clang
         
            "lseopkg z3-4.8.5-1-1-x86_64.eopkg" yields:
                 /usr/bin/z3
                 /usr/lib64/libz3.so.4.8
                 /usr/lib64/libz3.so.4.8.5.0
                 
            "lseopkg z3-devel-4.8.5-1-1-x86_64.eopkg" yields: 
                        /usr/include/z3++.h
                        /usr/include/z3.h
                        /usr/include/z3_algebraic.h
                        /usr/include/z3_api.h
                        /usr/include/z3_ast_containers.h
                        /usr/include/z3_fixedpoint.h
                        /usr/include/z3_fpa.h
                        /usr/include/z3_macros.h
                        /usr/include/z3_optimization.h
                        /usr/include/z3_polynomial.h
                        /usr/include/z3_rcf.h
                        /usr/include/z3_spacer.h
                        /usr/include/z3_v1.h
                        /usr/include/z3_version.h
                        /usr/lib64/cmake/z3/Z3Config.cmake
                        /usr/lib64/cmake/z3/Z3Targets-release.cmake
                        /usr/lib64/cmake/z3/Z3Targets.cmake
                        /usr/lib64/libz3.so

7) findlib: Dependency for LLVM, Clang.
            CANNOT INSTALL, Error message: "mkdir: cannot create directory ‘/etc/findlib’: Permission denied"
            
8) llvm-rocm: Compiles, creates package, but clang etc is missing later ???
9) rocm-device-libs: not compiling due to missing part in previous llv-rocm package
         
