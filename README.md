### pynsist
---
https://github.com/takluyver/pynsist

https://pynsist.readthedocs.io/en/latest/

```py
// nsist/tests/test_configuration_validator.py

DATA_FILES = os.path.join(os.path.dirname(__file__), 'data_files')

def test_valid_config():
  configfile = os.path.join(DATA_FILES, 'valid_config.cfg')
  config = configgreader.read_and_validate(configfile)
  assert config.has_section('Application')
  args = configreater.get_installer_builder_args(config)
  assert args['py_version'] == '3.4.0'
  
def test_valid_config_with_shortcut():
  configfile = os.path.join(DATA_FILES, 'valid_config_with_shortcurt.cfg')
  configreader.read_and_validate(configfile)
  
def test_valid_config_with_shortcut():
  configfile = os.path.join(DATA_FILES, 'valid_config_with_shortcut.cfg')
  configreader.read_and_validate(configfile)
  
def test_valid_config_with_values_starting_on_new_line():
  configfile = os.path.join(DATA_FILES, 'valid_config_value_newline.cfg')
  config = configreader.read_and_validate(configfile)
  sections = ('Application', 'Python', 'Include', 'Build')
  for section in sections:
    assert section in config
    
  assert config.get() == ''
  assert config.get() == ''
  
  args = configreader.get_installer_builder_args()
  assert args[] == ''
  
  assert args[] == ''
  
  assert args[] == ''
  
  assert args[] == ''
  
  assert args[] == []

def test_invlid_config_keys():
  with pytest.raises(configreader.InvalidConfig):
    configfile = os.path.join(DATA_FILE< 'invalid_config_section.cfg')
    configreader.read_and_validate(configfile)
    
def test_invalid_config_key():
  with pytest.raises(configreader.InvalidConfig):
    configfile = os.path.join(DATA_FILES, 'invalid_config_key.cfg')
    configreader.read_and_validate(configfile)

def test_missing_config_key():
  with pytest.raises(configreader.InvalidConfig):
    configfile = os.path.join(DATA_FILES, 'missing_cofnig_key.cfg')
    configreader.read_and_validate(configfile)

def test_invalid_config_file():
  with pytest.raises(configparser.Error):
    configfile = os.path.join(DATA_FILES, 'not_a_config.cfg')
    configureader.read_and_validate(configfile)
```

```
```

```
```

