# Vector Role

Устанавливает и настраивает Vector observability pipeline на CentOS 7/8.

## Требования

- CentOS 7/8
- Ansible >= 2.11
- Python 3.6+

## Переменные

| Переменная | Описание | Значение по умолчанию |
|------------|----------|----------------------|
| `vector_version` | Версия Vector | `0.21.1` |
| `vector_install_dir` | Директория установки | `/opt/vector` |
| `vector_config_dir` | Директория конфигурации | `/etc/vector` |
| `vector_user` | Пользователь для запуска | `vector` |

## Пример использования

```yaml
- hosts: vector
  become: true
  roles:
    - role: vector