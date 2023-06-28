### Usage
```bash
os-config generate-api-key
```

### Description
Generate an API key if device has `apiEndpoint` and `deviceApiKey(s)` doesn't already exist. 

If generated, write the key to `config.json`, where the change will be picked up by the Supervisor & VPN services.

### Observations & potential improvements
- `config_json.rs`
	- [ ] Unit tests
	- [ ] Generalized `get` & `set` methods for getting & setting individual or groups of config key-values
		- [ ] Insert as new key-value pair if defined in `os-config.json` schema but doesn't exist in `config.json`
		- [ ] Method for removal 
