# Changelog

## [1.3.0](https://github.com/antmelekhin/ansible-role-openssh/compare/v1.2.0...v1.3.0) (2023-08-22)


### Fixes

* add fqcn for all modules ([7874196](https://github.com/antmelekhin/ansible-role-openssh/commit/7874196dd2a34b5dd068de76f77fdd986a339cb5))


### Improvements

* distribution select ([bf084e1](https://github.com/antmelekhin/ansible-role-openssh/commit/bf084e19ca71310becc1e41f84e4eeb55ba236eb))


### Tests

* add tox ([1038302](https://github.com/antmelekhin/ansible-role-openssh/commit/10383023ff9efa6c3572b7fc7bb7e6bc1e25e487))
* fix box image ([6198aae](https://github.com/antmelekhin/ansible-role-openssh/commit/6198aaed0ccb6698953cb368fc321ac9513265df))

## [1.2.0](https://github.com/antmelekhin/ansible-role-openssh/compare/v1.1.1...v1.2.0) (2023-08-14)


### Continuous Integration

* update distros matrix ([0a09ec5](https://github.com/antmelekhin/ansible-role-openssh/commit/0a09ec5611868a185240ec0fcbc88cc262376897))


### Features

* add `Allow*` and `Deny*` directives to sshd_config ([fead95b](https://github.com/antmelekhin/ansible-role-openssh/commit/fead95be98e25058a58e3eba70eb69fe9ebed98d))


### Styles

* add quotes in notify name ([70dcdf6](https://github.com/antmelekhin/ansible-role-openssh/commit/70dcdf616c19a072c666ff857155aa1252a85897))

## [1.1.1](https://github.com/antmelekhin/ansible-role-openssh/compare/v1.1.0...v1.1.1) (2023-06-21)


### Fixes

* rm security task ([43d59dd](https://github.com/antmelekhin/ansible-role-openssh/commit/43d59dd2aeb66b616f6b339a4a35395c588ded5c))

## [1.1.0](https://github.com/antmelekhin/ansible-role-openssh/compare/v1.0.0...v1.1.0) (2023-06-21)


### Continuous Integration

* add `improv` releaseRule ([3eb828c](https://github.com/antmelekhin/ansible-role-openssh/commit/3eb828ca8b04e8db9581a579a1d5f47e87c2afc1))
* add `publish` and `release` workflows ([d7e71a5](https://github.com/antmelekhin/ansible-role-openssh/commit/d7e71a53a481ac4b41260503ce49277fe504ae49))


### Documentation

* update supported os ([3db5cc5](https://github.com/antmelekhin/ansible-role-openssh/commit/3db5cc54c00a36e683865b4970cbe753427d65f6))


### Fixes

* mv selinux setting to configure.yml ([b70f881](https://github.com/antmelekhin/ansible-role-openssh/commit/b70f881992e4339d6252525712448714cf9b6c06))
* mv windows firewall setting to configure.yml ([7bef392](https://github.com/antmelekhin/ansible-role-openssh/commit/7bef3929258082248d6d00653bc6b0f75db77dc5))
* rm firewalld task ([dd971c3](https://github.com/antmelekhin/ansible-role-openssh/commit/dd971c3427e129cdb472f591c5194c52dfbcd053))


### Improvements

* distribution select ([6d7f231](https://github.com/antmelekhin/ansible-role-openssh/commit/6d7f231780a686a186b6ad7319d73e57dafa249c))


### Styles

* add `openssh_sshd_host_keys_dir` variable ([3d6543e](https://github.com/antmelekhin/ansible-role-openssh/commit/3d6543e33310d658242f2e9f2b751eaf4a1fed66))
* rename service tasks ([9ee6b78](https://github.com/antmelekhin/ansible-role-openssh/commit/9ee6b787275182fc5cf9d48b8296c9daed7048c0))


### Tests

* fix linting rules ([86781d3](https://github.com/antmelekhin/ansible-role-openssh/commit/86781d3d32976ff0555fd5de558f9dbfd8ce63cd))
* update molecule scenarios ([a2a91dd](https://github.com/antmelekhin/ansible-role-openssh/commit/a2a91dd0c14ceecb6261d2c4dde15dcf07f23b8b))
