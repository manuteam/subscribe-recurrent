<template>
  <div class="card card-custom gutter-b mt-30">
    <div class="card-body">
      <div class="d-flex align-items-center flex-wrap">
        <div class="flex-grow-1">
          <div class="d-flex align-items-center justify-content-between flex-wrap">
            <div class="mr-3">
              {{ $t('Today') }}
            </div>
            <div class="my-lg-0 my-1">
              {{ $t('Tomorrow') }}
            </div>
          </div>
        </div>
      </div>

      <div class="separator separator-solid my-7"></div>

      <div class="d-flex align-items-center flex-wrap">

        <div class="d-flex align-items-center flex-lg-fill mr-5 my-1">
          <span class="mr-4">
            <div class="d-flex flex-column text-dark-75">
              <span class="font-wight-bolder font-size-sm">{{ $t('Earnings') }}</span>
              <span class="font-weight-bolder font-size-h5">{{ formatPrice(subscriberCounts) }}</span>
            </div>
          </span>
        </div>
        <div class="d-flex align-items-center flex-lg-fill mr-5 my-1">
          <span class="mr-4">
            <i class="flaticon-piggy-bank icon-2x text-muted font-weight-bold"></i>
            <div class="d-flex flex-column text-dark-75">
              <span class="font-wight-bolder font-size-sm">{{ $t('Subscribers') }}</span>
              <span class="font-weight-bolder font-size-h5">{{ subscriberCounts }}</span>
            </div>
          </span>
        </div>
        <div class="d-flex align-items-center flex-lg-fill mr-5 my-1">
          <span class="mr-4">
            <i class="flaticon-piggy-bank icon-2x text-muted font-weight-bold"></i>
            <div class="d-flex flex-column text-dark-75">
              <span class="font-wight-bolder font-size-sm">{{ $t('Debt') }}</span>
              <span class="font-weight-bolder font-size-h5">{{ formatPrice(debt) }}</span>
            </div>
          </span>
        </div>
        <div class="d-flex align-items-center flex-lg-fill mr-5 my-1">
          <span class="mr-4">
            <i class="flaticon-piggy-bank icon-2x text-muted font-weight-bold"></i>
            <div class="d-flex flex-column text-dark-75">
              <span class="font-wight-bolder font-size-sm">{{ $t('TodayToPay') }}</span>
              <span class="font-weight-bolder font-size-h5">{{ subscriberTodayToPay }}</span>
            </div>
          </span>
        </div>
        <div class="d-flex align-items-center flex-lg-fill mr-5 my-1">
          <span class="mr-4">
            <i class="flaticon-piggy-bank icon-2x text-muted font-weight-bold"></i>
            <div class="d-flex flex-column text-dark-75">
              <span class="font-wight-bolder font-size-sm">{{ $t('TomorrowToPay') }}</span>
              <span class="font-weight-bolder font-size-h5">{{ subscriberTomorrowToPay }}</span>
            </div>
          </span>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardMain",
  data() {
    return {
      currency: '$',
      subscriberCounts: 100,
      subscriberTodayToPay: 5,
      subscriberTomorrowToPay: 7,
      earningsCount: 320000,
      debt: 3000
    }
  },
  methods: {
    formatPrice (value) {
      return this.currency + value
    }
  }
}
</script>

<style scoped>

</style>
