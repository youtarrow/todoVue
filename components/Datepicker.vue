<template>
  <form class="" @submit.prevent>
    <div class="v-calendar">
      <v-date-picker v-model="range" mode="dateTime" :masks="masks" is-range>
        <template v-slot="{ inputValue, inputEvents, isDragging }">
          <div class="d-flex v-calendar__inputArea">
            <div class="itemeBox relative d-flex align-items-center">
              <svg
                class=""
                fill="none"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"
                ></path>
              </svg>
              <input
                class=""
                :class="isDragging ? 'text-gray-600' : 'text-gray-900'"
                :value="inputValue.start"
                v-on="inputEvents.start"
              />
            </div>
            <span
              class="itemeBox d-flex justify-content-center align-items-center"
            >
              →
            </span>
            <div class="itemeBox relative d-flex align-items-center">
              <svg
                class=""
                fill="none"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"
                ></path>
              </svg>
              <input
                class=""
                :class="isDragging ? 'text-gray-600' : 'text-gray-900'"
                :value="inputValue.end"
                v-on="inputEvents.end"
              />
            </div>
          </div>
        </template>
      </v-date-picker>
    </div>
  </form>
</template>

<script>
const now = new Date()
// eslint-disable-next-line no-unused-vars
const year = now.getFullYear()
// eslint-disable-next-line no-unused-vars
const months = now.getMonth()
// eslint-disable-next-line no-unused-vars
const date = now.getDate()
const today = new Date(year, months, date)

export default {
  data() {
    return {
      range: {
        start: today,
        end: today,
      },
      masks: {
        input: 'YYYY-MM-DD h:mm A',
      },
    }
  },
}
</script>

<style lang="scss">
.v-calendar {
  &__inputArea {
    .itemeBox {
      &:nth-child(1),
      &:nth-child(3) {
        width: auto;
        svg {
          position: absolute;
          left: 4px;
          width: 30px;
        }
      }
      &:nth-child(2) {
        width: 7%;
        font-size: 25px;
      }
      input {
        border: 1px solid gray;
        padding: 10px 10px 10px 50px;
        width: 100%;
      }
    }
  }
}
</style>
