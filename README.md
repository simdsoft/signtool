# signtool
The code sign tool compatible with microsoft  signtool.exe


# references
https://www.codeproject.com/Articles/1271890/EV-Code-Signing-with-a-hardware-token


# count of signatures
```cpp
struct _WINTRUST_DATA {
  // ...
#if (NTDDI_VERSION >= NTDDI_WIN8)
  struct WINTRUST_SIGNATURE_SETTINGS_    *pSignatureSettings;
#endif // #if (NTDDI_VERSION >= NTDDI_WIN8)
};

struct _CRYPT_PROVIDER_SIGSTATE {
  // ...
  DWORD cSecondarySigs;       //A count of the secondary signatures
  // ...
}
```

refer to: https://famellee.wordpress.com/2016/09/08/retrieve-digital-signatures-using-wintrust/
