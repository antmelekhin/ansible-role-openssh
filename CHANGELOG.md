# Changelog

## [1.7.1](https://github.com/antmelekhin/ansible-role-openssh/compare/v1.7.0...v1.7.1) (2024-10-01)


### Code Refactoring

* update `SyslogFacility` and `LogLevel` variables ([e67ba12](https://github.com/antmelekhin/ansible-role-openssh/commit/e67ba122b34b17d1d0b201d6d1555b8cf1d20cd3))

## [1.7.0](https://github.com/antmelekhin/ansible-role-openssh/compare/v1.6.0...v1.7.0) (2024-09-28)


### Continuous Integration

* use `ubuntu-22.04` instead of `ubuntu-latest` ([d646437](https://github.com/antmelekhin/ansible-role-openssh/commit/d646437222ceb5264908e04cabbd7281f3c2ea16))


### Features

* add `noble` support ([#9](https://github.com/antmelekhin/ansible-role-openssh/issues/9)) ([2384947](https://github.com/antmelekhin/ansible-role-openssh/commit/238494778b6a5548278491b17c9b4f57f49c2486))

## [1.6.0](https://github.com/antmelekhin/ansible-role-openssh/compare/v1.5.0...v1.6.0) (2024-08-10)


### Features

* add `meta/argument_specs.yml` file ([#8](https://github.com/antmelekhin/ansible-role-openssh/issues/8)) ([c8c8f80](https://github.com/antmelekhin/ansible-role-openssh/commit/c8c8f80a215f889cabc7f3aa50b60463ba70376a))

## [1.5.0](https://github.com/antmelekhin/ansible-role-openssh/compare/v1.4.0...v1.5.0) (2024-08-07)


### Features

* add `fedora` and `amazonlinux` support ([#7](https://github.com/antmelekhin/ansible-role-openssh/issues/7)) ([06d3c45](https://github.com/antmelekhin/ansible-role-openssh/commit/06d3c4522969b9d857315e55f25d69042213d713))

## [1.4.0](https://github.com/antmelekhin/ansible-role-openssh/compare/v1.3.3...v1.4.0) (2024-08-07)


### Improvements

* merge OS-specific variables into the `vars/main.yml` file ([#6](https://github.com/antmelekhin/ansible-role-openssh/issues/6)) ([44cbc1b](https://github.com/antmelekhin/ansible-role-openssh/commit/44cbc1b22d8378acb8063e09be99007971cb7162))


### Styles

* update common role style ([#5](https://github.com/antmelekhin/ansible-role-openssh/issues/5)) ([67cb812](https://github.com/antmelekhin/ansible-role-openssh/commit/67cb8123235e0af5df184c2cefd00d2d51b1a010))

## [1.3.3](https://github.com/antmelekhin/ansible-role-openssh/compare/v1.3.2...v1.3.3) (2024-05-13)


### Documentation

* **README:** update variables documentation ([a4607e1](https://github.com/antmelekhin/ansible-role-openssh/commit/a4607e127c423d7b4c172f11ee13f5db28529575))


### Styles

* rename tasks ([4c45ae6](https://github.com/antmelekhin/ansible-role-openssh/commit/4c45ae6116851e9ef2cad1fdfb7ee36b1623cad0))

## [1.3.2](https://github.com/antmelekhin/ansible-role-openssh/compare/v1.3.1...v1.3.2) (2024-05-01)


### Documentation

* **README:** fixed examples view for Ansible Galaxy ([98a027b](https://github.com/antmelekhin/ansible-role-openssh/commit/98a027bad6195365349caf662c3e3002e23bbeac))


### Fixes

* fixed running a role in check_mode ([e55dfde](https://github.com/antmelekhin/ansible-role-openssh/commit/e55dfde0bc9fb7a0e27c3ad714b020e02222519a))


### Styles

* add newline to end of file ([67b4ffb](https://github.com/antmelekhin/ansible-role-openssh/commit/67b4ffb69b89fb2d6d6db58c7e14c88a7f83d32f))
* use double underline in register variable ([55d12b4](https://github.com/antmelekhin/ansible-role-openssh/commit/55d12b494e686e8bd01f3dfb4b1581d87b60868d))


### Tests

* add .tox as ignore ([5848152](https://github.com/antmelekhin/ansible-role-openssh/commit/5848152a42347d5e920786ee5b4fcebe94e1bf2e))
* add role_name prefix to instance name ([39b5742](https://github.com/antmelekhin/ansible-role-openssh/commit/39b5742da866a612ce729613c38a4f07df8fa656))
* run linters in its own workflow ([2d0f63a](https://github.com/antmelekhin/ansible-role-openssh/commit/2d0f63a5627bcff21734e7b268b96a863f32746f))

## [1.3.1](https://github.com/antmelekhin/ansible-role-openssh/compare/v1.3.0...v1.3.1) (2024-04-22)


### Code Refactoring

* minor fixes ([#4](https://github.com/antmelekhin/ansible-role-openssh/issues/4)) ([12db0bc](https://github.com/antmelekhin/ansible-role-openssh/commit/12db0bc4d1f48cd12f3514b5631403de79f43a63))


### Continuous Integration

* update release rules ([b830687](https://github.com/antmelekhin/ansible-role-openssh/commit/b8306874b24fcf7df433cebbb6c39629bba97396))
* update workflows ([b6250ec](https://github.com/antmelekhin/ansible-role-openssh/commit/b6250ec4b08c19aa535721af8f0906843c5cedae))
* **fix:** add requirements.yml that resolvs dependencies for molecule action ([#3](https://github.com/antmelekhin/ansible-role-openssh/issues/3)) ([5fbb0d2](https://github.com/antmelekhin/ansible-role-openssh/commit/5fbb0d2e556f9caf948ae5c09bb2c19f38944c18))


### Tests

* fix molecule container name ([5979445](https://github.com/antmelekhin/ansible-role-openssh/commit/59794450d137e887838446c2a9bdb59ddca720df))

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
