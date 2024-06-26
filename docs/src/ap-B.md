# 附录B：实验所用到的其余专业前置知识

### C++ STL

C++ 标准模板库（Standard Template Library，STL）是 C++ 标准库的一部分，提供了一系列的模板类和函数，用于实现常用的数据结构和算法。STL 的设计理念是“泛型编程”，即通过模板技术使得算法和数据结构可以独立于具体的数据类型。STL 主要包含以下几个组件：

#### 1. 容器（Containers）

容器是用来存储数据的对象，STL 提供了多种容器，每种容器都有其特定的用途和性能特点。常见的容器包括：

- **向量（vector）**：动态数组，支持随机访问。
- **列表（list）**：双向链表，支持高效的插入和删除操作。
- **双端队列（deque）**：双端队列，支持两端高效插入和删除。
- **集合（set）**：存储不重复元素的集合，内部通常使用平衡二叉树实现。
- **多重集合（multiset）**：与 set 类似，但允许元素重复。
- **映射（map）**：键值对的集合，内部通常使用平衡二叉树实现。
- **多重映射（multimap）**：与 map 类似，但允许键重复。
- **栈（stack）**：后进先出（LIFO）的数据结构。
- **队列（queue）**：先进先出（FIFO）的数据结构。
- **优先队列（priority_queue）**：元素出队顺序由优先级决定。

#### 2. 迭代器（Iterators）

迭代器是连接算法和容器的桥梁，它提供了一种统一的方式来访问容器中的元素。STL 中的迭代器分为几种类型，包括输入迭代器、输出迭代器、前向迭代器、双向迭代器和随机访问迭代器。

#### 3. 算法（Algorithms）

STL 提供了一系列的算法，这些算法可以作用于不同类型的容器。常见的算法包括排序（sort）、搜索（find）、合并（merge）、复制（copy）、替换（replace）等。这些算法通常都是通过迭代器来操作容器中的元素。

#### 4. 函数对象（Function Objects）

函数对象，也称为仿函数，是重载了函数调用操作符 `()` 的类对象。它们可以像普通函数一样被调用，同时也可以保存状态或者进行类型检查。STL 中的许多算法都接受函数对象作为参数，以实现自定义的行为。

#### 5. 适配器（Adapters）

适配器是一种特殊的容器或函数对象，它们通过改变其他容器或函数对象的接口来提供新的接口。例如，栈和队列就是通过适配器实现的，它们分别基于向量和双端队列，但提供了不同的接口。

6. #### **分配器（Allocators）**

分配器负责管理容器中元素的内存分配和释放。STL 默认使用 `std::allocator`，但用户也可以自定义分配器以满足特定的内存管理需求。

STL 的设计使得数据结构和算法的实现与具体的数据类型无关，这大大提高了代码的复用性和灵活性。通过使用 STL，开发者可以更加专注于算法的设计和实现，而不必重复编写基本的数据结构和算法。

[菜鸟教程 C++](https://www.runoob.com/cplusplus/cpp-tutorial.html)

### Shell

Shell 是一种命令行解释器，它为用户提供了一个与操作系统内核进行交互的界面。通过 shell，用户可以输入命令，执行程序，管理文件和系统等。Shell 不仅是一个命令解释器，还是一个强大的编程环境，允许用户编写脚本来自动化复杂的任务。

#### 常见的 Shell 类型

1. **Bash (Bourne Again SHell)**：这是最常用的 shell，它是 GNU 项目的一部分，广泛用于 Linux 和 macOS 系统。
2. **sh (Bourne Shell)**：由 Stephen Bourne 在 AT&T 开发，是许多其他 shell 的基础。
3. **csh (C Shell)**：语法类似于 C 语言，提供了一些额外的功能，如命令历史和别名。
4. **tcsh (TENEX C Shell)**：csh 的增强版本，增加了命令行编辑和命令补全等功能。
5. **zsh (Z Shell)**：一个功能强大的 shell，集成了许多其他 shell 的特性，并提供了许多增强功能。
6. **fish (Friendly Interactive SHell)**：设计用于提供用户友好的体验，包括自动建议和语法高亮。

#### Shell 的基本功能

1. **命令执行**：用户可以直接在 shell 中输入命令，shell 会解释并执行这些命令。
2. **文件系统导航**：使用 `cd`、`ls`、`pwd` 等命令来浏览和管理文件系统。
3. **重定向和管道**：允许用户将命令的输入输出重定向到文件或其他命令，使用 `|` 符号可以将一个命令的输出作为另一个命令的输入。
4. **环境变量**：用户可以设置环境变量来影响命令的行为，例如 `PATH` 变量定义了命令的搜索路径。
5. **脚本编程**：用户可以编写 shell 脚本来执行一系列命令，脚本可以包含条件判断、循环、函数等编程结构。
6. **作业控制**：用户可以启动、停止、恢复和终止后台作业。

#### Shell 脚本编程

Shell 脚本是一种简单的脚本语言，它允许用户将一系列命令组合成一个文件，以便自动执行。脚本可以包含变量、控制结构（如 `if`、`for`、`while`）、函数和命令。以下是一个简单的 Bash 脚本示例：

```shell
#!/bin/bash
# 这是一个简单的 Bash 脚本

echo "Hello, World!"

# 使用变量
name="Alice"
echo "Hello, $name!"

# 使用条件判断
if [ "$name" == "Alice" ]; then
    echo "Welcome, Alice!"
fi

# 使用循环
for i in {1..5}; do
    echo "Count: $i"
done
```

要运行这个脚本，首先需要给它执行权限，然后可以直接运行：

```shell
chmod +x script.sh
./script.sh
```

Shell 是系统管理员和开发人员的重要工具，它提供了强大的自动化和定制能力。通过学习和使用 shell，用户可以更高效地管理和操作计算机系统。

### YAML

YAML（"YAML Ain't Markup Language" 的递归缩写）是一种人类可读的数据序列化标准，广泛用于配置文件、数据交换、对象持久化等领域。YAML 的设计目标是使数据在不同编程语言之间交换变得简单，同时保持良好的可读性和简洁性。

#### YAML 的基本语法

1. **缩进**：YAML 使用缩进来表示数据结构中的层次关系。通常使用空格（推荐使用两个空格），不建议使用制表符。
2. **冒号**：用于表示键值对，冒号后面通常跟着一个空格。
3. **短横线**：用于表示列表项，短横线后面通常跟着一个空格。
4. **注释**：使用井号 `#` 表示单行注释。
5. **引用**：可以使用 `&` 定义锚点，使用 `*` 引用锚点。
6. **字符串**：字符串不需要引号，但如果包含特殊字符或需要跨行，可以使用单引号或双引号。
7. **布尔值**：可以使用 `true`、`false`、`yes`、`no`、`on`、`off` 等。
8. **空值**：使用 `null` 或 `~` 表示。

#### YAML 示例

以下是一个简单的 YAML 文件示例：

```yaml
# 这是一个 YAML 示例文件

name: John Doe
age: 30
is_student: false
hobbies:
  - reading
  - hiking
  - coding
contact:
  email: john.doe@example.com
  phone: 123-456-7890
address:
  street: 123 Main St
  city: Anytown
  state: CA
  zip: 12345
```

在这个示例中，`name`、`age` 和 `is_student` 是键值对，`hobbies` 是一个列表，`contact` 和 `address` 是嵌套的键值对。

#### YAML 的应用

YAML 常用于配置文件，因为它比 XML 和 JSON 更加简洁和易读。许多流行的软件和框架，如 Docker、Kubernetes、Ansible、Spring Boot 等，都使用 YAML 作为配置文件格式。

#### 注意事项

- YAML 文件不区分大小写，但通常约定使用小写字母。
- 避免在 YAML 文件中使用特殊字符，除非它们被正确转义。
- 在处理 YAML 文件时，确保使用支持 YAML 标准的解析器。

YAML 是一种灵活且强大的数据序列化格式，它使得配置文件和数据交换更加简单和直观。通过学习和使用 YAML，开发者可以更有效地管理配置和数据。
