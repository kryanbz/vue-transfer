<template>
  <div>
    <b-row>
      <b-col></b-col>
    <b-col cols = 7>
<b-navbar toggleable="lg" type="light" variant="light">
    <b-navbar-brand href="#">Transfer Center</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
       
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-form>
          <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
          <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
        </b-nav-form>


          
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</b-col>
<b-col></b-col>
</b-row>
<b-container class="bv-example-row">
  <b-row>
    <b-col cols = 8>
      <p> 
       <img src=" https://www.ub.edu.bz/wp-content/uploads/2016/08/UB_logo_2017.png" style = "float:left"><br>
          Faculty of Science and Technology <br>
          Math, Physics and IT Department <br>
          ASSOCIATE DEGREE IN IT SEQUENCE  <br>
          Effective Semester 2019-1-2020-1 
      </p>
    </b-col>
    <b-col>
<b-dropdown text="Feeder Institution" block>
    <b-dropdown-item href="#">Sacred Heart Junior College</b-dropdown-item>
    <b-dropdown-item href="#">Saint Johns College</b-dropdown-item>
  </b-dropdown>


    </b-col>
    </b-row>

  <b-row>
    <b-col cols = 8>

    <template>
  <div>
    <b-table :items="items" :fields="fields" striped responsive="sm">
      <template #cell(show_details)="row">
        <b-button  size="sm" @click="row.toggleDetails">
          {{ row.detailsShowing ? 'Hide' : 'Show'}} Details
        </b-button>


      </template>

      <template #row-details="row">
        <b-card>
          <b-row class="mb-2">
            <b-col sm="3" class="text-sm-right"><b>Semester:</b></b-col>
            <b-col>{{ row.item.semester }}</b-col>
          </b-row>

          <b-row class="mb-2">
            <b-col sm="3" class="text-sm-right"><b>Course Description:</b></b-col>
            <b-col>{{ row.item.description }}</b-col>
          </b-row>

          <b-button size="sm" @click="row.toggleDetails">Hide Details</b-button>
        </b-card>
      </template>
    </b-table>
  </div>
</template>
  
    
    
    
    
    
    
    </b-col>
   

    <b-col>  
   
  <b-row>
  <p> Course Outlines </p>
  </b-row>   
   
  
  <b-button a href="CMPS1134.pdf" class="button in-left2" target="_blank">Course Outline</b-button>
  
  
  
  
  </b-col>

  </b-row>
</b-container>


    
  </div>


  
</template>

<script>
  export default {
    data() {
      return {
        fields: ['course_code', 'course_name', 'show_details'],
        items: [
          { description: "This course is an introduction to the fundamentals of Computer Science that will provide students with a foundation for future courses in Computer Science. The course is a broad survey of the discipline through topics that allow students to understand the capabilities of computer systems in terms of: the computer architecture; operating systems and computer networks; software and software development; data organization and visualization; and the potential of computing machines", semester: "2020-2", course_code: 'CMPS1134', course_name: 'Fundamentals of Computing' },
          { description: "Course Description", semester: "2020-2", course_code: 'CMPS1131', course_name: 'Principles of Programming I' },
          {
            description: "Course Description",
            semester: "2020-2",
            course_code: 'MATH1151',
            course_name: 'Algebra',
            _showDetails: true
          },
          { description: "Course Description", semester: "2020-2", course_code: 'MATH1201', course_name: 'Trigonometry' }
        ]
      }
    }
  }
</script>