<template>
  <main class="container--main">
    <section class="search-channel">
      <div class="search-channel__wrapper">
        <div class="input-block input-block--name">
          <label for="id-channel">Название канала или ссылка на канал</label>
          <input class="input" id="id-channel" placeholder="Ввести название канала или ссылку...">
        </div>
        <button class="button" type="button">Расширенный поиск</button>
      </div>
      <div class="advanced-search__wrapper">
        <div class="advanced-search-inputs">
          <div class="advanced-search__column">
            <div class="input-block">
              <label for="category">Категория</label>
              <input class="input" id="category" placeholder="Ввести категорию">
            </div>
            <div class="input-block">
              <label for="description">Описание</label>
              <input class="input" id="description" placeholder="Ввести описание">
            </div>
            <div class="input-block">
              <label for="type-channel">Тип канала</label>
              <select class="input" id="type-channel">
                <option>Выбрать тип канала</option>
              </select>
            </div>
            <div class="input-block input-block--checkbox">
              <input type="checkbox" class="checkbox__input visually-hidden" id="verified">
              <label for="verified">Только проверенные каналы</label>
            </div>
          </div>
          <div class="advanced-search__column">
            <div class="input-block">
              <label for="subscriber-from">Подписчики</label>
              <div class="input-wrapper">
                <div class="input-group">
                  <span class="input-group-text">от</span>
                  <input class="input input--filter" id="subscriber-from" placeholder="500">
                </div>
                <div class="input-group">
                  <span class="input-group-text">до</span>
                  <input class="input input--filter" id="subscriber-before" placeholder="10 000">
                </div>
              </div>
            </div>
            <div class="input-block">
              <label for="er-from">ER%</label>
              <div class="input-wrapper">
                <div class="input-group">
                  <span class="input-group-text">от</span>
                  <input class="input input--filter" id="er-from" placeholder="1">
                </div>
                <div class="input-group">
                  <span class="input-group-text">до</span>
                  <input class="input input--filter" id="er-before" placeholder="25">
                </div>
              </div>
            </div>
            <div class="input-block">
              <label for="subscriber-from">Упоминаний за неделю</label>
              <div class="input-wrapper">
                <div class="input-group">
                  <span class="input-group-text">от</span>
                  <input class="input input--filter" id="reference-from" placeholder="150">
                </div>
                <div class="input-group">
                  <span class="input-group-text">до</span>
                  <input class="input input--filter" id="reference-before" placeholder="500">
                </div>
              </div>
            </div>
            <div class="input-block input-block--checkbox">
              <input type="checkbox" class="checkbox__input visually-hidden" id="sale">
              <label for="sale">Только каналы со скидкой</label>
            </div>
          </div>
          <div class="advanced-search__column">
            <div class="input-block">
              <label for="views-post-from">Просмотров на пост</label>
              <div class="input-wrapper">
                <div class="input-group">
                  <span class="input-group-text">от</span>
                  <input class="input input--filter" id="views-post-from" placeholder="500">
                </div>
                <div class="input-group">
                  <span class="input-group-text">до</span>
                  <input class="input input--filter" id="views-post-before" placeholder="10 000">
                </div>
              </div>
            </div>
            <div class="input-block">
              <label for="views-tg-from">Просмотры Telegraph</label>
              <div class="input-wrapper">
                <div class="input-group">
                  <span class="input-group-text">от</span>
                  <input class="input input--filter" id="views-tg-from" placeholder="100">
                </div>
                <div class="input-group">
                  <span class="input-group-text">до</span>
                  <input class="input input--filter" id="views-tg-before" placeholder="500">
                </div>
              </div>
            </div>
            <div class="input-block">
              <label for="number-reviews-from">Количетво отзывов</label>
              <div class="input-wrapper">
                <div class="input-group">
                  <span class="input-group-text">от</span>
                  <input class="input input--filter" id="number-reviews-from" placeholder="100">
                </div>
                <div class="input-group">
                  <span class="input-group-text">до</span>
                  <input class="input input--filter" id="number-reviews-before" placeholder="500">
                </div>
              </div>
            </div>
            <div class="input-block">
              <label for="post-price-from">Цена за пост</label>
              <div class="input-wrapper">
                <div class="input-group">
                  <span class="input-group-text">от</span>
                  <input class="input input--filter" id="post-price-from" placeholder="1500">
                </div>
                <div class="input-group">
                  <span class="input-group-text">до</span>
                  <input class="input input--filter" id="post-price-before" placeholder="5000">
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="buttons-search">
          <div class="button-wrapper">
            <p class="button-head">Категории</p>
            <div class="button-container">
              <p class="button-search-active">Музыка</p>
              <p>Бизнес</p>
              <p>Фильмы</p>
              <p>Видео</p>
              <p>Ужасы</p>
              <p>Смех</p>
              <p>Юмор</p>
            </div>
          </div>
          <div class="button-wrapper">
            <p class="button-head">Период</p>
            <div class="button-container">
              <p class="button-search-active">Вчера</p>
              <p>День назад</p>
              <p>7 дней</p>
              <p>30 дней</p>
              <p>Год</p>
            </div>
          </div>
        </div>
      </div>
      <div class="paginator">
      </div>
    </section>
    <section>
      <table class="channel-table">
        <tr class="channel-table__headline">
          <td>
            <a class="channel-table__link" href="#">Название</a>
          </td>
          <td>
            <a class="channel-table__link" href="#">Подписчики</a>
          </td>
          <td>
            <a class="channel-table__link" href="#">Прирост</a>
            <span class="channel-table__headline-time">сегодня неделя</span>
          </td>
          <td>
            <a class="channel-table__link" href="#">Охват</a>
            <span class="channel-table__headline-time">среднее за сутки</span>
          </td>
          <td>
            <a  class="channel-table__link" href="#">ER%</a>
          </td>
          <td>
            <a class="channel-table__link" href="#">Отзывы</a>
            <span class="channel-table__headline-time"></span>
          </td>
          <td>
            <a class="channel-table__link" href="#"></a>
          </td>
        </tr>
        <tr v-for="channel in channels">
          <td class="main-info">
            <div>
              <a href="#">
                <img class="main-info__photo" :src="channel.realImg" width="55" height="55">
              </a>
            </div>
            <div class="main-info__text-wrapper">
              <p class="main-info__name">{{ channel.name }}</p>
              <a class="main-info__tg" href="#">@{{ channel.username }}</a>
              <span class="main-info__section">Раздел канала</span>
            </div>
          </td>
          <td class="channel-table__numbers">
            <p>{{ channel.subscribers_count }}</p>
          </td>
          <td class="channel-table__numbers">
            <p class="channel-table__plus">{{ channel.his24 }}</p>
            <p class="channel-table__minus">{{ channel.his7 }}</p>
          </td>
          <td class="channel-table__numbers">
            <p>{{ channel.viewAll }}</p>
            <p>{{ channel.view24 }}</p>
          </td>
          <td class="channel-table__numbers">
            <p>{{ channel.er }}</p>
          </td>
          <td class="channel-table__numbers">
            <p></p>
            <p></p>
          </td>
          <td class="channel-table__numbers">
            <p></p>
          </td>
        </tr>
      </table>
      <div class="paginator">
        <paginate
                :page-count="pagesCount"
                :prev-text="'Prev'"
                :click-handler="pageClickHandler"
                :next-text="'Next'"
                :hide-prev-next="false"
                :page-class="'paginator__item'"
                :next-link-class="'paginator__item'"
                :prev-link-class="'paginator__item'"
                :force-page="currentPage"
                :active-class="'paginator__item--current'"
                :container-class="'paginator__list'">
        </paginate>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: 'Channels',
  props: {
  },
  data: function() {
    return {
      'channels': [],
      'pagesCount': 0,
      'currentPage': 1
    }
  },
  methods: {
    getData: function (page) {
      fetch('http://89.108.64.223/api/v1/list?page=' + page).then((response) => response.json())
        .then((channels) => {
          this.pagesCount = channels.pageCount;
          this.channels = channels.list;
        });
    },
    pageClickHandler: function (page) {
      this.getData(page);
      this.currentPage = page;
    }
  },
  created: function () {
    this.getData(0);
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.paginator__list li:first-child,
.paginator__list li:last-child {
  display: none;
}
</style>
