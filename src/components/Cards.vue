<template>
  <div class="q-pa-lg">
    <div class="row">
      <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
        <div>Available balance</div>
        <div class="row">
          <div class="col-lg-1 col-md-1 col-sm-2 col-xs-3">
            <q-badge class="q-mt-sm" align="middle" color="as-green">S$</q-badge>
          </div>
          <div class="col-lg-11 col-md-11 col-sm-10 col-xs-9 text-h6">3,000</div>
        </div>
      </div>
      <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6" align="right">
        <q-btn color="as-blue" icon="add_circle" label="New card" no-caps/>
      </div>
    </div>
    <div class="q-mt-lg">
      <q-tabs
        v-model="tab"
        dense
        class="text-grey"
        active-color="black"
        indicator-color="primary"
        align="left"
        no-caps
        >
        <q-tab name="debit" label="My debit cards" />
        <q-tab name="company" label="All company cards" />
      </q-tabs>

      

      <q-tab-panels v-model="tab" animated>
        <q-tab-panel name="debit" class="q-px-xs">
          <q-card class="q-pa-md row">
            <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12 q-pa-md">
              <div align="right">
                <q-btn icon="visibility" label="Show card number" flat color="as-green" no-caps></q-btn>
              </div>
              <div class="bg-as-green q-pa-md debit-card">
                <div align="right">
                  <img src="../assets/AspireLogo.svg" style="height:20px"/>
                </div>
                <div class="text-h6 text-white q-mt-md">Mark Henry</div>
                <div class="q-mt-md">
                  <q-badge rounded color="white" class="q-mr-xs"/>
                  <q-badge rounded color="white" class="q-mx-xs"/>
                  <q-badge rounded color="white" class="q-mx-xs"/>
                  <q-badge rounded color="white" class="q-ml-xs q-mr-lg"/>
                  <q-badge rounded color="white" class="q-mr-xs"/>
                  <q-badge rounded color="white" class="q-mx-xs"/>
                  <q-badge rounded color="white" class="q-mx-xs"/>
                  <q-badge rounded color="white" class="q-mx-xs q-mr-lg"/>
                  <q-badge rounded color="white" class="q-mx-xs"/>
                  <q-badge rounded color="white" class="q-mx-xs"/>
                  <q-badge rounded color="white" class="q-mx-xs"/>
                  <q-badge rounded color="white" class="q-mx-xs q-mr-lg"/>
                  <q-badge rounded color="as-green" label="2" />
                  <q-badge rounded color="as-green" label="0" />
                  <q-badge rounded color="as-green" label="2" />
                  <q-badge rounded color="as-green" label="0" />
                </div>
                <div class="row q-mt-md">
                  <div class="col-4 text-white">Thru: 12/20</div>
                  <div class="col-4 text-white">CVV: ***</div>
                  <div class="col-4"></div>
                </div>
                <div align="right">
                  <img src="../assets/VisaLogo.svg" style="height:20px"/>
                </div>
              </div>
              <div class="card-option q-mt-lg q-pa-sm">
                <div align="center">
                  <img src="../assets/FreezeCard.svg" style="height:20px"/>
                  <div>Freeze</div>
                  <div>card</div>
                </div>
                <div align="center">
                  <img src="../assets/SetSpendLimit.svg" style="height:20px"/>
                  <div>Set spend</div>
                  <div>limit</div>
                </div>
                <div align="center">
                  <img src="../assets/GPay.svg" style="height:20px"/>
                  <div>Add to</div>
                  <div>GPay</div>
                </div>
                <div align="center">
                  <img src="../assets/ReplaceCard.svg" style="height:20px"/>
                  <div>Replace</div>
                  <div>card</div>
                </div>
                <div align="center">
                  <img src="../assets/DeactivateCard.svg" style="height:20px"/>
                  <div>Cancel</div>
                  <div>card</div>
                </div>
              </div>
            </div>
            <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12 q-pa-md">
              <div class="q-pa-md q-mt-lg card-details row">
                <div class="col-2"><img src="../assets/Group.svg" style="height:20px"/></div>
                <div class="col-8">Card details</div>
                <div class="col-2" align="right"><img src="../assets/down-arrow.svg" style="height:20px"/></div>
              </div>
              <div class="q-pa-md q-mt-lg card-details row">
                <div class="col-2"><img src="../assets/swap.svg" style="height:20px"/></div>
                <div class="col-8">Recent transactions</div>
                <div class="col-2" align="right"><img src="../assets/up-arrow.svg" style="height:20px"/></div>
              </div>
              <div>
                <q-list bordered>
                  <q-item clickable v-ripple>
                    <q-item-section avatar>
                      <q-avatar color="as-light-blue">
                        <img src="../assets/file-storage.svg" style="height:14px"/>
                      </q-avatar>
                    </q-item-section>
                    <q-item-section>
                      <q-item-label>Hamleys</q-item-label>
                      <q-item-label caption>20 May 2020</q-item-label>
                      <q-item-label class="text-as-blue">
                        <q-avatar color="as-blue" size="20px">
                          <img src="../assets/business-and-finance.svg" style="height:8px"/>
                        </q-avatar>
                        Refund on debit card
                      </q-item-label>
                    </q-item-section>
                    <q-item-section side top>
                      <q-item-label class="text-as-green">+ S$ 150</q-item-label>
                    </q-item-section>
                  </q-item>
                  <q-separator inset/>
                  <q-item clickable v-ripple>
                    <q-item-section avatar>
                      <q-avatar color="as-light-green">
                        <img src="../assets/flights.svg" style="height:14px"/>
                      </q-avatar>
                    </q-item-section>
                    <q-item-section>
                      <q-item-label>Hamleys</q-item-label>
                      <q-item-label caption>20 May 2020</q-item-label>
                      <q-item-label class="text-as-blue">
                        <q-avatar color="as-blue" size="20px">
                          <img src="../assets/business-and-finance.svg" style="height:8px"/>
                        </q-avatar>
                        Charged to debit card
                      </q-item-label>
                    </q-item-section>
                    <q-item-section side top>
                      <q-item-label class="text-black">- S$ 150</q-item-label>
                    </q-item-section>
                  </q-item>
                  <q-separator inset/>
                  <q-item clickable v-ripple>
                    <q-item-section avatar>
                      <q-avatar color="as-light-red">
                        <img src="../assets/megaphone.svg" style="height:14px"/>
                      </q-avatar>
                    </q-item-section>
                    <q-item-section>
                      <q-item-label>Hamleys</q-item-label>
                      <q-item-label caption>20 May 2020</q-item-label>
                      <q-item-label class="text-as-blue">
                        <q-avatar color="as-blue" size="20px">
                          <img src="../assets/business-and-finance.svg" style="height:8px"/>
                        </q-avatar>
                        Charged to debit card
                      </q-item-label>
                    </q-item-section>
                    <q-item-section side top>
                      <q-item-label class="text-black">- S$ 150</q-item-label>
                    </q-item-section>
                  </q-item>
                  <q-separator inset/>
                  <q-item clickable v-ripple>
                    <q-item-section avatar>
                      <q-avatar color="as-light-blue">
                        <img src="../assets/file-storage.svg" style="height:14px"/>
                      </q-avatar>
                    </q-item-section>
                    <q-item-section>
                      <q-item-label>Hamleys</q-item-label>
                      <q-item-label caption>20 May 2020</q-item-label>
                      <q-item-label class="text-as-blue">
                        <q-avatar color="as-blue" size="20px">
                          <img src="../assets/business-and-finance.svg" style="height:8px"/>
                        </q-avatar>
                        Charged to debit card
                      </q-item-label>
                    </q-item-section>
                    <q-item-section side top>
                      <q-item-label class="text-black">- S$ 150</q-item-label>
                    </q-item-section>
                  </q-item>
                </q-list>
              </div>
            </div>

          </q-card>
        </q-tab-panel>

        <q-tab-panel name="company">
          
        </q-tab-panel>
      </q-tab-panels>
    </div>
  </div>
</template>
<script>

export default {
  created(){
    console.log("QUAS",this.$q.screen.xs)
  },
  
  data () {
    return {
      tab: 'debit'
    }
  },
  methods:{
  }
}
</script>
<style lang="scss">
.debit-card{
  border-radius: 8px;
}

.card-option{
  display: flex;
  justify-content: space-around;
  background: #EDF3FF;
  border-radius: 8px;
  font-size: 11px;
  color: #0C365A;
}
.card-details{
  background: #F5F9FF;
  border-radius: 8px;
  color: #0C365A;
}

</style>