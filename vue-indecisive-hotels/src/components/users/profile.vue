<template>

<v-container style="max-width: 1200px" py-0 px-0>
  <v-layout row>
    <v-flex xs12 sm10 md8 offset-sm1 offset-md2 pa-5>
    
      <v-card style="opacity: 0.7;">
        <v-toolbar dark color="brown darken-2">
          
          <v-toolbar-title>Account Details</v-toolbar-title>
          <v-spacer></v-spacer>
          </v-toolbar>
        <v-list two-line>
          <v-list-tile>
          	<v-list-tile-title>Name: {name}
          	</v-list-tile-title>
          	 <v-dialog v-model="nameDialog" persistent max-width="500px">
      <v-btn color="brown darken-2" dark slot="activator">Edit Name</v-btn>
      <v-card>
        <v-card-title>
          <span class="headline">Edit Name</span>
        </v-card-title>
        <v-card-text>
          <v-container grid-list-md>
            <v-layout wrap>
              <v-flex xs12 sm6 md4>
                <v-text-field label="New first name" required></v-text-field>
              </v-flex>
              <v-flex xs12 sm6 md4>
                <v-text-field label="New last name" hint="example of helper text only on focus"></v-text-field>
              </v-flex>
            </v-layout>
          </v-container>
          <small>*indicates required field</small>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="brown darken-2" flat @click.native="nameDialog = false">Close</v-btn>
          <v-btn color="brown darken-2" flat @click.native="nameDialog = false">Save</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
        </v-list-tile>
        </v-list>
        <v-list two-line>
          <v-list-tile>
          	<v-list-tile-title>Email: {email}
          	</v-list-tile-title>
          	<v-dialog v-model="emailDialog" persistent max-width="500px">
      <v-btn color="brown darken-2" dark slot="activator">Edit Email</v-btn>
      <v-card>
        <v-card-title>
          <span class="headline">Edit Email</span>
        </v-card-title>
        <v-card-text>
          <v-container grid-list-md>
            <v-layout wrap>
              <v-flex xs12 sm12>
                <v-text-field label="New email" required></v-text-field>
              </v-flex>
              <v-flex xs12 sm12>
                <v-text-field label="Confirm new email" ></v-text-field>
              </v-flex>
            </v-layout>
          </v-container>
         
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="brown darken-2" flat @click.native="emailDialog = false">Close</v-btn>
          <v-btn color="brown darken-2" flat @click.native="emailDialog = false">Save</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
        </v-list-tile>
        </v-list> 
        <v-list two-line>
          <v-list-tile>
          	<v-list-tile-title>Password: Set
          	</v-list-tile-title>
          	<v-dialog v-model="passwordDialog" persistent max-width="500px">
      <v-btn color="brown darken-2" dark slot="activator">Edit Password</v-btn>
      <v-card>
        <v-card-title>
          <span class="headline">Edit Password</span>
        </v-card-title>
        <v-card-text>
          <v-container grid-list-md>
            <v-layout wrap>
              <v-flex xs12 sm12>
                <v-text-field label="Current Password" required></v-text-field>
              </v-flex>
              <v-flex xs12 sm12>
                <v-text-field label="New Password" required></v-text-field>
              </v-flex>
              <v-flex xs12 sm12>
                <v-text-field label="Confirm New Password" ></v-text-field>
              </v-flex>
            </v-layout>
          </v-container>
         
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="brown darken-2" flat @click.native="passwordDialog = false">Close</v-btn>
          <v-btn color="brown darken-2" flat @click.native="passwordDialog = false">Save</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
        </v-list-tile>
        </v-list> 
        
      </v-card>
      <br><br><br>
      <v-card style="opacity: 0.7;">
        <v-toolbar dark color="brown darken-2">
          
          <v-toolbar-title>Card Information</v-toolbar-title>
          <v-spacer></v-spacer>
          </v-toolbar>
        <v-list two-line>
          <v-list-tile>
          	<v-list-tile-title>Card ending in 1234
          	</v-list-tile-title>
          	 <v-dialog v-model="cardDialog" persistent max-width="500px">
      <v-btn color="brown darken-2" dark slot="activator">Edit Card Number</v-btn>
      <v-card>
        <v-card-title>
          <span class="headline">Edit Card Number</span>
        </v-card-title>
        <v-card-text>
          <v-container grid-list-md>
            <v-layout wrap>
              <v-flex xs12 sm12>
                <v-text-field label="New Card Number" required></v-text-field>
              </v-flex>
              <v-flex xs12 sm12>
                <v-text-field label="Confirm New Card Number" hint="example of helper text only on focus"></v-text-field>
              </v-flex>
            </v-layout>
          </v-container>
          <small>*indicates required field</small>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="brown darken-2" flat @click.native="cardDialog = false">Close</v-btn>
          <v-btn color="brown darken-2" flat @click.native="cardDialog = false">Save</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
        </v-list-tile>
        </v-list>
        <v-list two-line>
          <v-list-tile>
          	<v-list-tile-title>Expiration: {expiration}
          	</v-list-tile-title>
          	<v-dialog v-model="cardExp" persistent max-width="500px">
      <v-btn color="brown darken-2" dark slot="activator">Edit Expiration</v-btn>
      <v-card>
        <v-card-title>
          <span class="headline">Edit Expiration</span>
        </v-card-title>
        <v-card-text>
          <v-container grid-list-md>
            <v-layout wrap>
              <v-flex xs12 sm6>
                <v-select
                  label="Month"
                  required
                  :items="['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December']"
                ></v-select>
              </v-flex>
              <v-flex xs12 sm6>
                <v-select
                  label="Year"
                  required
                  :items="['2018', '2019', '2020', '2021', '2022', '2023', '2024', '2025', '2026', '2027']"
                ></v-select>
              </v-flex>
            </v-layout>
          </v-container>
         
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="brown darken-2" flat @click.native="cardExp = false">Close</v-btn>
          <v-btn color="brown darken-2" flat @click.native="cardExp = false">Save</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
        </v-list-tile>
        </v-list> 
        <v-list two-line>
          <v-list-tile>
          	<v-list-tile-title>Card Security Code: Set
          	</v-list-tile-title>
          	<v-dialog v-model="cardSecurtyCode" persistent max-width="500px">
      <v-btn color="brown darken-2" dark slot="activator">Edit Security Code</v-btn>
      <v-card>
        <v-card-title>
          <span class="headline">Edit Security Code</span>
        </v-card-title>
        <v-card-text>
          <v-container grid-list-md>
            <v-layout wrap>
              <v-flex xs12 sm12>
                <v-text-field label="New Security Code" required></v-text-field>
              </v-flex>
              <v-flex xs12 sm12>
                <v-text-field label="Confirm New Security Code" ></v-text-field>
              </v-flex>
            </v-layout>
          </v-container>
         
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="brown darken-2" flat @click.native="cardSecurtyCode = false">Close</v-btn>
          <v-btn color="brown darken-2" flat @click.native="cardSecurtyCode = false">Save</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
        </v-list-tile>
        </v-list>
      </v-card>

      <br><br><br>
      <v-card style="opacity: 0.7;">
        <v-toolbar dark color="brown darken-2">
          
          <v-toolbar-title>Billing Information</v-toolbar-title>
          <v-spacer></v-spacer>
          </v-toolbar>
        <v-list two-line>
          <v-list-tile>
            <v-list-tile-title>Address: {address}
            
            </v-list-tile-title>
            <v-card-text>
            <br>1 Washington Sq
            <br>San Jose, CA 95192
            </v-card-text>
            
            
             <v-dialog v-model="addressDialog" persistent max-width="500px">
      <v-btn color="brown darken-2" dark slot="activator">Edit Address</v-btn>
      <v-card>
        <v-card-title>
          <span class="headline">Edit Address</span>
        </v-card-title>
        <v-card-text>
          <v-container grid-list>
            <v-layout wrap>
              <v-flex xs12 sm12>
                <v-text-field label="Street" required></v-text-field>
              </v-flex>
              <v-flex xs12 sm7>
                <v-text-field label="City"  required></v-text-field>
              </v-flex>
              <v-flex xs12 sm5>
                <v-text-field label="State"  required></v-text-field>
                <v-flex xs12 sm12>
                <v-text-field label="Zip"  required></v-text-field>
              </v-flex>
              </v-flex>
            </v-layout>
          </v-container>
          
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="brown darken-2" flat @click.native="addressDialog = false">Close</v-btn>
          <v-btn color="brown darken-2" flat @click.native="addressDialog = false">Save</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
        </v-list-tile>
        </v-list>
        
    </v-dialog>
        </v-list-tile>
        </v-list> 
        
      </v-card>
    </v-flex>
  </v-layout>
</v-container>

</template>
<script>
  export default {
    data: () => ({
      nameDialog: false,
      emailDialog: false,
      passwordDialog: false,
      cardDialog: false,
      cardExp: false,
      cardSecurtyCode: false,
      addressDialog: false
    })
  }
</script>