### 管理 cache

查看当前的 cache 状态：

```bash
huggingface-cli scan-cache
```

### 缓存指定仓库

```python
import typer
from typing_extensions import Annotated
from tenacity import retry, stop_after_attempt, wait_fixed

from huggingface_hub import snapshot_download



@retry(stop=stop_after_attempt(10), wait=wait_fixed(5))
def cache(repo_id: Annotated[str, typer.Argument(..., help="仓库 ID")]):
    snapshot_download(repo_id=repo_id)
    
if __name__ == "__main__":
    typer.run(cache)
```