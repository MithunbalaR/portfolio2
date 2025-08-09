# Portfolio Customization Guide

## 🎯 Quick Start Customization

### 1. Personal Information
Edit `config/portfolio-data.ts` and update the `personalInfo` object:

\`\`\`typescript
export const personalInfo = {
  name: "Your Full Name",           // Replace with your name
  title: "Your Professional Title", // e.g., "Frontend Developer", "UI/UX Designer"
  email: "your.email@example.com",  // Your contact email
  phone: "+1 (555) 123-4567",      // Your phone number
  location: "Your City, State",     // Your location
  
  bio: [
    "Write your first paragraph about yourself here...",
    "Add a second paragraph about your interests and goals..."
  ],
  
  profileImage: "/path-to-your-photo.jpg", // Add your actual photo
  resumeUrl: "/your-resume.pdf"             // Link to your resume
}
\`\`\`

### 2. Social Media Links
Update the `socialLinks` array:

\`\`\`typescript
export const socialLinks = [
  {
    name: "GitHub",
    url: "https://github.com/YOUR_USERNAME",     // Your GitHub profile
    icon: Github
  },
  {
    name: "LinkedIn", 
    url: "https://linkedin.com/in/YOUR_USERNAME", // Your LinkedIn profile
    icon: Linkedin
  },
  // Add or remove social platforms as needed
]
\`\`\`

### 3. Skills Section
Update your skills and proficiency levels (0-100):

\`\`\`typescript
export const skills = [
  { name: "React", level: 90 },        // Adjust level based on your expertise
  { name: "JavaScript", level: 95 },   // Add your actual skills
  { name: "Python", level: 80 },       // Remove skills you don't have
  // Add more skills:
  // { name: "Vue.js", level: 75 },
  // { name: "Docker", level: 65 },
]
\`\`\`

### 4. Projects Portfolio
Replace with your actual projects:

\`\`\`typescript
export const projects = [
  {
    title: "Your Project Name",
    description: "Brief description of what the project does and its key features",
    image: "/images/your-project-screenshot.jpg", // Add actual screenshots
    tech: ["React", "Node.js", "MongoDB"],        // Technologies you used
    github: "https://github.com/you/project-repo", // Your GitHub repo
    live: "https://your-project-demo.com",         // Live demo URL
    featured: true // Set to true for your best projects
  },
  // Add more projects...
]
\`\`\`

### 5. Work Experience
Update with your actual work history:

\`\`\`typescript
export const experiences = [
  {
    title: "Your Job Title",
    company: "Company Name",
    period: "Start Date - End Date", // e.g., "Jan 2022 - Present"
    description: "What you accomplished in this role, key responsibilities, and impact",
    technologies: ["Tech", "Stack", "You", "Used"] // Optional
  },
  // Add more experiences...
]
\`\`\`

## 📁 Adding Your Images

### Profile Photo
1. Add your professional headshot to the `public/images/` folder
2. Update the `profileImage` path in `personalInfo`:
   \`\`\`typescript
   profileImage: "/images/your-photo.jpg"
   \`\`\`

### Project Screenshots
1. Add project screenshots to `public/images/projects/`
2. Update each project's `image` field:
   \`\`\`typescript
   image: "/images/projects/your-project.jpg"
   \`\`\`

### Resume/CV
1. Add your resume PDF to the `public/` folder
2. Update the `resumeUrl` in `personalInfo`:
   \`\`\`typescript
   resumeUrl: "/your-resume.pdf"
   \`\`\`

## 🎨 Color Customization

### Changing the Color Scheme
Edit the gradient colors in `app/page.tsx`:

\`\`\`typescript
// Hero section gradient
className="bg-gradient-to-r from-blue-400 via-green-400 to-purple-400"

// Button gradients  
className="bg-gradient-to-r from-blue-500 to-green-500"

// Background gradient
className="bg-gradient-to-br from-slate-900 via-blue-900 to-slate-900"
\`\`\`

### Custom Colors
You can also update `tailwind.config.ts` to add your brand colors:

\`\`\`typescript
module.exports = {
  theme: {
    extend: {
      colors: {
        'brand-primary': '#your-color',
        'brand-secondary': '#your-color',
      }
    }
  }
}
\`\`\`

## 📱 Content Tips

### Writing Effective Descriptions
- **Projects**: Focus on the problem solved and impact
- **Experience**: Use action verbs and quantify achievements
- **Bio**: Keep it conversational but professional
- **Skills**: Be honest about your proficiency levels

### SEO Optimization
- Use descriptive project titles
- Include relevant keywords in descriptions
- Add alt text for images
- Update the page title and meta description

## 🚀 Deployment Checklist

Before deploying:
- [ ] Replace all placeholder content with your information
- [ ] Add your actual photos and project screenshots
- [ ] Test all external links (GitHub, LinkedIn, live demos)
- [ ] Update contact information
- [ ] Add your resume/CV file
- [ ] Test on mobile devices
- [ ] Check for typos and grammar

## 🔧 Advanced Customization

### Adding New Sections
To add a new section (e.g., "Testimonials"):

1. Add the section data to `portfolio-data.ts`
2. Create the section component in `app/page.tsx`
3. Add navigation link to the nav array
4. Update the scroll functionality

### Changing Animations
Framer Motion animations can be customized by modifying the `initial`, `animate`, and `transition` props in the motion components.

### Adding a Blog Section
Consider adding a blog section by creating a new route and connecting to a CMS like Contentful or Sanity.
