# hse_hw4_scRNA_seq

## Нормализация данных
Данные были нормализованы методом TPM, обычный метод TPM задается следующей формулой

$$
    TPM_i = \frac{\frac{q_i}{l_i}}{\sum\frac{q_j}{j_j}}\cdot 10^6
$$

Где $q_i$ - риды попавшие на транскрипцию, а $l_i$ - длина транскрипции, однако нам длина неизвестна, так что мы будем использовать следующую формулу

$$
    TPM_i = \frac{q_i}{\sum\ q_j}\cdot 10^6
$$


## Heatmap
Как мы видим, несмотря на отсутсвие длин, мы получили такой же Heatmap, как и ожидалось
![Alt text](/img/heatmap-marked.png "Title")

На картинке можно заметить несколько (~5) кластеров клеток, это свидительствует о том, что клетки каждого кластера принадлежат одному типу. 

## UMAP и PCA
Также были визуализированы UMAP и PCA, используя [anndata](https://anndata.readthedocs.io/en/latest/) и [scanpy](https://scanpy.readthedocs.io/en/stable/)

![Alt text](/img/pca.png "Title")

![Alt text](/img/umap.png "Title")


Тут мы разбили данные по группам cTEC, mTEC-I, mTEC-II, mTEC-III, mTEC-IV, тем самым понизив размерность данных и получив деление на группы

