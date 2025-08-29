# Pacman Search Project (CS188)

## Yêu cầu
- Python 3.x
- Đã cài đặt thư viện tiêu chuẩn (không cần cài thêm package bên ngoài)
- Hệ điều hành: Linux/MacOS/WSL (Windows chạy được nhưng nên dùng WSL/Ubuntu)

## Cấu trúc quan trọng
- `search.py` — nơi bạn cài đặt DFS, BFS, UCS, A*
- `searchAgents.py` — agent dùng các giải thuật trong `search.py`
- `util.py` — cấu trúc dữ liệu hỗ trợ (Stack, Queue, PriorityQueue,…)
- `autograder.py` — script tự động chấm điểm
- `test_cases/` — chứa test case cho từng câu hỏi

## Chạy test với autograder
- Chạy toàn bộ:
```bash
python autograder.py
```

- Chạy từng câu:
```bash
python autograder.py -q q1    # DFS
python autograder.py -q q2    # BFS
python autograder.py -q q3    # UCS
python autograder.py -q q4    # A*
python autograder.py -q q5    # CornersProblem
python autograder.py -q q6    # Food heuristic
python autograder.py -q q7    # FoodSearch heuristic nâng cao
python autograder.py -q q8    # ClosestDotSearch
```

- Chạy nhanh, không mở giao diện đồ họa:
```bash
python autograder.py --no-graphics
```

## Chạy Pacman trực tiếp
Bạn có thể quan sát Pacman chạy bằng cách dùng `pacman.py`:

- DFS:
```bash
python pacman.py -l tinyMaze -p SearchAgent -a fn=depthFirstSearch
```

- BFS:
```bash
python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs
```

- UCS:
```bash
python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs
```

- A* với heuristic Manhattan:
```bash
python pacman.py -l bigMaze -z 0.5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic
```

- CornersProblem:
```bash
python pacman.py -l mediumCorners -p AStarCornersAgent
```

- FoodSearch:
```bash
python pacman.py -l trickySearch -p AStarFoodSearchAgent
```

- ClosestDotSearch:
```bash
python pacman.py -l mediumSearch -p ClosestDotSearchAgent
```

## Mẹo
- `-z 0.5` thu nhỏ kích thước maze để dễ quan sát
- `--frameTime 0` tăng tốc chạy
- `--pacman NullGraphics` tắt render (chỉ chạy logic)

---

✅ Với các lệnh trên, bạn có thể test cả **autograder** lẫn **chạy trực tiếp Pacman** để quan sát.  
